<template>
  <div class="min-h-screen bg-gray-50 py-12">
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Header -->
      <div class="text-center mb-12">
        <h1 class="text-4xl font-bold text-gray-900 mb-4">Book Your Training Session</h1>
        <p class="text-xl text-gray-600">
          Fill out the form below to schedule your personalized training session with our expert trainers.
        </p>
      </div>

      <!-- Booking Form -->
      <form @submit.prevent="submitBooking" class="bg-white rounded-xl shadow-lg p-8 mb-8">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <!-- Personal Information -->
          <div class="md:col-span-2">
            <h3 class="text-lg font-semibold text-gray-900 mb-4 border-b border-gray-200 pb-2">
              Personal Information
            </h3>
          </div>
          
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Full Name *</label>
            <input
              v-model="bookingForm.fullName"
              type="text"
              required
              class="input-field"
              placeholder="Enter your full name"
            />
          </div>
          
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Email Address *</label>
            <input
              v-model="bookingForm.email"
              type="email"
              required
              class="input-field"
              placeholder="Enter your email"
            />
          </div>
          
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Phone Number *</label>
            <input
              v-model="bookingForm.phone"
              type="tel"
              required
              class="input-field"
              placeholder="Enter your phone number"
            />
          </div>
          
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Password *</label>
            <input
              v-model="bookingForm.password"
              type="password"
              required
              class="input-field"
              placeholder="Create a password"
            />
          </div>
          
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Age</label>
            <input
              v-model="bookingForm.age"
              type="number"
              min="16"
              max="100"
              class="input-field"
              placeholder="Enter your age"
            />
          </div>
          
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Weight (kg)</label>
            <input
              v-model="bookingForm.weight"
              type="number"
              min="30"
              max="300"
              step="0.1"
              class="input-field"
              placeholder="Enter your weight"
            />
          </div>

          <!-- Session Details -->
          <div class="md:col-span-2">
            <h3 class="text-lg font-semibold text-gray-900 mb-4 border-b border-gray-200 pb-2 mt-8">
              Session Details
            </h3>
          </div>
          
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Preferred Date *</label>
            <input
              v-model="bookingForm.preferredDate"
              type="date"
              required
              class="input-field"
              :min="new Date().toISOString().split('T')[0]"
            />
          </div>
          
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Preferred Time *</label>
            <input
              v-model="bookingForm.preferredTime"
              type="time"
              required
              class="input-field"
            />
          </div>
          
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Session Duration</label>
            <select v-model="bookingForm.duration" class="input-field">
              <option value="">Select duration</option>
              <option value="30">30 minutes</option>
              <option value="45">45 minutes</option>
              <option value="60">1 hour</option>
              <option value="90">1.5 hours</option>
              <option value="120">2 hours</option>
            </select>
          </div>
          
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">Training Type</label>
            <select v-model="bookingForm.trainingType" class="input-field">
              <option value="">Select training type</option>
              <option value="strength">Strength Training</option>
              <option value="cardio">Cardio</option>
              <option value="flexibility">Flexibility & Yoga</option>
              <option value="hiit">HIIT</option>
              <option value="weight-loss">Weight Loss</option>
              <option value="muscle-gain">Muscle Gain</option>
              <option value="rehabilitation">Rehabilitation</option>
            </select>
          </div>

          <!-- Fitness Level & Goals -->
          <div class="md:col-span-2">
            <h3 class="text-lg font-semibold text-gray-900 mb-4 border-b border-gray-200 pb-2 mt-8">
              Fitness Level & Goals
            </h3>
          </div>
          
          <div class="md:col-span-2">
            <label class="block text-sm font-medium text-gray-700 mb-2">Fitness Level</label>
            <div class="flex flex-wrap gap-4">
              <label class="flex items-center">
                <input
                  v-model="bookingForm.fitnessLevel"
                  type="radio"
                  value="beginner"
                  class="mr-2 text-primary-600"
                />
                Beginner
              </label>
              <label class="flex items-center">
                <input
                  v-model="bookingForm.fitnessLevel"
                  type="radio"
                  value="intermediate"
                  class="mr-2 text-primary-600"
                />
                Intermediate
              </label>
              <label class="flex items-center">
                <input
                  v-model="bookingForm.fitnessLevel"
                  type="radio"
                  value="advanced"
                  class="mr-2 text-primary-600"
                />
                Advanced
              </label>
            </div>
          </div>
          
          <div class="md:col-span-2">
            <label class="block text-sm font-medium text-gray-700 mb-2">Fitness Goals (Select all that apply)</label>
            <div class="grid grid-cols-2 md:grid-cols-3 gap-3">
              <label class="flex items-center">
                <input
                  v-model="bookingForm.fitnessGoals"
                  type="checkbox"
                  value="weight-loss"
                  class="mr-2 text-primary-600"
                />
                Weight Loss
              </label>
              <label class="flex items-center">
                <input
                  v-model="bookingForm.fitnessGoals"
                  type="checkbox"
                  value="muscle-gain"
                  class="mr-2 text-primary-600"
                />
                Muscle Gain
              </label>
              <label class="flex items-center">
                <input
                  v-model="bookingForm.fitnessGoals"
                  type="checkbox"
                  value="endurance"
                  class="mr-2 text-primary-600"
                />
                Endurance
              </label>
              <label class="flex items-center">
                <input
                  v-model="bookingForm.fitnessGoals"
                  type="checkbox"
                  value="flexibility"
                  class="mr-2 text-primary-600"
                />
                Flexibility
              </label>
              <label class="flex items-center">
                <input
                  v-model="bookingForm.fitnessGoals"
                  type="checkbox"
                  value="general-fitness"
                  class="mr-2 text-primary-600"
                />
                General Fitness
              </label>
              <label class="flex items-center">
                <input
                  v-model="bookingForm.fitnessGoals"
                  type="checkbox"
                  value="sports-performance"
                  class="mr-2 text-primary-600"
                />
                Sports Performance
              </label>
            </div>
          </div>

          <!-- Previous Experience Section -->
          <div class="md:col-span-2">
            <h3 class="text-lg font-semibold text-gray-900 mb-4 border-b border-gray-200 pb-2 mt-8">
              Previous Gym Experience
            </h3>
            <p class="text-gray-600 mb-4">
              Help us understand your fitness background to provide a better training experience.
            </p>
            
            <button
              type="button"
              @click="openExperienceModal"
              class="btn-secondary mb-4"
            >
              Add Previous Experience
            </button>
            
            <!-- Display Previous Experience -->
            <div v-if="previousExperiences.length > 0" class="space-y-3">
              <div
                v-for="(experience, index) in previousExperiences"
                :key="index"
                class="bg-gray-50 p-4 rounded-lg border border-gray-200"
              >
                <div class="flex justify-between items-start">
                  <div>
                    <p class="font-medium text-gray-900">{{ experience.gymName }}</p>
                    <p class="text-sm text-gray-600">{{ experience.duration }} - {{ experience.workoutType }}</p>
                    <p v-if="experience.comments" class="text-sm text-gray-600 mt-1">{{ experience.comments }}</p>
                  </div>
                  <button
                    type="button"
                    @click="removeExperience(index)"
                    class="text-red-600 hover:text-red-800 text-sm"
                  >
                    Remove
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- Additional Information -->
          <div class="md:col-span-2">
            <h3 class="text-lg font-semibold text-gray-900 mb-4 border-b border-gray-200 pb-2 mt-8">
              Additional Information
            </h3>
          </div>
          
          <div class="md:col-span-2">
            <label class="block text-sm font-medium text-gray-700 mb-2">Medical Conditions or Injuries</label>
            <textarea
              v-model="bookingForm.medicalInfo"
              rows="3"
              class="input-field resize-none"
              placeholder="Please describe any medical conditions, injuries, or limitations we should know about..."
            ></textarea>
          </div>
          
          <div class="md:col-span-2">
            <label class="block text-sm font-medium text-gray-700 mb-2">Profile Picture</label>
            <input
              type="file"
              accept="image/*"
              @change="handleFileUpload"
              class="input-field"
            />
            <p class="text-sm text-gray-500 mt-1">Upload a profile picture (optional)</p>
          </div>
          
          <div class="md:col-span-2">
            <label class="block text-sm font-medium text-gray-700 mb-2">Additional Comments</label>
            <textarea
              v-model="bookingForm.additionalComments"
              rows="4"
              class="input-field resize-none"
              placeholder="Any other information you'd like to share..."
            ></textarea>
          </div>
        </div>

        <!-- Submit Button -->
        <div class="mt-8 text-center">
          <button type="submit" class="btn-primary text-lg px-8 py-4">
            Book Training Session
          </button>
        </div>
      </form>

      <!-- Form Summary -->
      <div v-if="showSummary" class="bg-white rounded-xl shadow-lg p-8">
        <h3 class="text-2xl font-bold text-gray-900 mb-6 text-center">Booking Summary</h3>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <div>
            <h4 class="font-semibold text-gray-900 mb-3">Personal Information</h4>
            <p><strong>Name:</strong> {{ bookingForm.fullName }}</p>
            <p><strong>Email:</strong> {{ bookingForm.email }}</p>
            <p><strong>Phone:</strong> {{ bookingForm.phone }}</p>
            <p v-if="bookingForm.age"><strong>Age:</strong> {{ bookingForm.age }}</p>
            <p v-if="bookingForm.weight"><strong>Weight:</strong> {{ bookingForm.weight }} kg</p>
          </div>
          <div>
            <h4 class="font-semibold text-gray-900 mb-3">Session Details</h4>
            <p><strong>Date:</strong> {{ formatDate(bookingForm.preferredDate) }}</p>
            <p><strong>Time:</strong> {{ bookingForm.preferredTime }}</p>
            <p v-if="bookingForm.duration"><strong>Duration:</strong> {{ bookingForm.duration }} minutes</p>
            <p v-if="bookingForm.trainingType"><strong>Type:</strong> {{ formatTrainingType(bookingForm.trainingType) }}</p>
            <p><strong>Fitness Level:</strong> {{ formatFitnessLevel(bookingForm.fitnessLevel) }}</p>
          </div>
        </div>
        
        <div v-if="previousExperiences.length > 0" class="mt-6">
          <h4 class="font-semibold text-gray-900 mb-3">Previous Experience</h4>
          <div class="space-y-2">
            <div v-for="(experience, index) in previousExperiences" :key="index" class="bg-gray-50 p-3 rounded">
              <p><strong>{{ experience.gymName }}</strong> - {{ experience.duration }} ({{ experience.workoutType }})</p>
              <p v-if="experience.comments" class="text-sm text-gray-600">{{ experience.comments }}</p>
            </div>
          </div>
        </div>
        
        <div class="mt-6 text-center">
          <button @click="showSummary = false" class="btn-secondary">
            Edit Booking
          </button>
        </div>
      </div>
    </div>

    <!-- Previous Experience Modal -->
    <Modal
      :is-open="experienceModalOpen"
      title="Add Previous Gym Experience"
      confirm-text="Add Experience"
      @close="closeExperienceModal"
      @confirm="addExperience"
    >
      <div class="space-y-4">
        <div>
          <label class="block text-sm font-medium text-gray-700 mb-2">Gym Name *</label>
          <input
            v-model="newExperience.gymName"
            type="text"
            required
            class="input-field"
            placeholder="Enter gym name"
          />
        </div>
        
        <div>
          <label class="block text-sm font-medium text-gray-700 mb-2">Duration *</label>
          <input
            v-model="newExperience.duration"
            type="text"
            required
            class="input-field"
            placeholder="e.g., 6 months, 2 years"
          />
        </div>
        
        <div>
          <label class="block text-sm font-medium text-gray-700 mb-2">Workout Type *</label>
          <input
            v-model="newExperience.workoutType"
            type="text"
            required
            class="input-field"
            placeholder="e.g., Strength training, Cardio, etc."
          />
        </div>
        
        <div>
          <label class="block text-sm font-medium text-gray-700 mb-2">Comments</label>
          <textarea
            v-model="newExperience.comments"
            rows="3"
            class="input-field resize-none"
            placeholder="Additional details about your experience..."
          ></textarea>
        </div>
      </div>
    </Modal>
  </div>
</template>

<script>
import Modal from '../components/Modal.vue'

export default {
  name: 'Booking',
  components: {
    Modal
  },
  data() {
    return {
      bookingForm: {
        fullName: '',
        email: '',
        phone: '',
        password: '',
        age: '',
        weight: '',
        preferredDate: '',
        preferredTime: '',
        duration: '',
        trainingType: '',
        fitnessLevel: '',
        fitnessGoals: [],
        medicalInfo: '',
        additionalComments: ''
      },
      previousExperiences: [],
      experienceModalOpen: false,
      newExperience: {
        gymName: '',
        duration: '',
        workoutType: '',
        comments: ''
      },
      showSummary: false
    }
  },
  methods: {
    openExperienceModal() {
      this.experienceModalOpen = true
      this.newExperience = {
        gymName: '',
        duration: '',
        workoutType: '',
        comments: ''
      }
    },
    
    closeExperienceModal() {
      this.experienceModalOpen = false
    },
    
    addExperience() {
      if (!this.newExperience.gymName || !this.newExperience.duration || !this.newExperience.workoutType) {
        return
      }
      
      this.previousExperiences.push({
        gymName: this.newExperience.gymName,
        duration: this.newExperience.duration,
        workoutType: this.newExperience.workoutType,
        comments: this.newExperience.comments
      })
      
      this.closeExperienceModal()
    },
    
    removeExperience(index) {
      this.previousExperiences.splice(index, 1)
    },
    
    handleFileUpload(event) {
      const file = event.target.files[0]
      if (file) {
        console.log('File uploaded:', file.name)
      }
    },
    
    submitBooking() {
      // Validate required fields
      if (!this.bookingForm.fullName || !this.bookingForm.email || !this.bookingForm.phone || 
          !this.bookingForm.password || !this.bookingForm.preferredDate || !this.bookingForm.preferredTime) {
        alert('Please fill in all required fields.')
        return
      }
      
      // Show summary
      this.showSummary = true
      
      // Scroll to summary
      this.$nextTick(() => {
        document.querySelector('.bg-white.rounded-xl.shadow-lg.p-8:last-of-type').scrollIntoView({
          behavior: 'smooth'
        })
      })
    },
    
    formatDate(dateString) {
      if (!dateString) return ''
      return new Date(dateString).toLocaleDateString('en-US', {
        weekday: 'long',
        year: 'numeric',
        month: 'long',
        day: 'numeric'
      })
    },
    
    formatTrainingType(type) {
      const types = {
        'strength': 'Strength Training',
        'cardio': 'Cardio',
        'flexibility': 'Flexibility & Yoga',
        'hiit': 'HIIT',
        'weight-loss': 'Weight Loss',
        'muscle-gain': 'Muscle Gain',
        'rehabilitation': 'Rehabilitation'
      }
      return types[type] || type
    },
    
    formatFitnessLevel(level) {
      const levels = {
        'beginner': 'Beginner',
        'intermediate': 'Intermediate',
        'advanced': 'Advanced'
      }
      return levels[level] || level
    }
  }
}
</script>
