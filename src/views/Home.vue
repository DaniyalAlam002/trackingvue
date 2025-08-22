<template>
  <div class="min-h-screen">
    <!-- Hero Section -->
    <section class="relative bg-gradient-to-br from-primary-600 via-primary-700 to-primary-800 text-white py-20 lg:py-32">
      <div class="absolute inset-0 bg-black bg-opacity-20"></div>
      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
          Transform Your Life
          <span class="block text-primary-200">With FitLife Gym</span>
        </h1>
        <p class="text-xl md:text-2xl mb-8 text-primary-100 max-w-3xl mx-auto">
          Join thousands of members who have achieved their fitness goals with our expert trainers and state-of-the-art equipment.
        </p>
        
        <!-- Phone Number in Hero -->
        <div class="flex items-center justify-center space-x-2 mb-8 text-primary-100">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20">
            <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"/>
          </svg>
          <span class="text-2xl font-bold">(555) 123-4567</span>
        </div>
        
        <router-link to="/book" class="btn-primary text-lg px-8 py-4 inline-block">
          Book Your Training Session
        </router-link>
      </div>
    </section>

    <!-- Features Section -->
    <section class="py-20 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            Why Choose FitLife Gym?
          </h2>
          <p class="text-xl text-gray-600 max-w-2xl mx-auto">
            We provide everything you need to achieve your fitness goals
          </p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="card text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Expert Trainers</h3>
            <p class="text-gray-600">Certified professionals with years of experience in fitness and nutrition.</p>
          </div>
          
          <div class="card text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Modern Equipment</h3>
            <p class="text-gray-600">State-of-the-art machines and free weights for every type of workout.</p>
          </div>
          
          <div class="card text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Flexible Hours</h3>
            <p class="text-gray-600">Open 24/7 to fit your busy schedule and lifestyle.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Newsletter Section -->
    <section class="py-20 bg-gray-50">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
          Stay Updated
        </h2>
        <p class="text-xl text-gray-600 mb-8">
          Get the latest fitness tips, class schedules, and exclusive offers delivered to your inbox.
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4 max-w-md mx-auto">
          <input
            v-model="newsletterEmail"
            type="email"
            placeholder="Enter your email"
            class="input-field flex-grow"
          />
          <button
            @click="subscribeNewsletter"
            class="btn-primary whitespace-nowrap"
          >
            Subscribe
          </button>
        </div>
        
        <p v-if="newsletterMessage" class="mt-4 text-sm" :class="newsletterMessageClass">
          {{ newsletterMessage }}
        </p>
      </div>
    </section>

    <!-- Contact Section -->
    <section class="py-20 bg-white">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            Get In Touch
          </h2>
          <p class="text-xl text-gray-600">
            Have questions? We'd love to hear from you. Send us a message and we'll respond as soon as possible.
          </p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div>
            <h3 class="text-xl font-semibold text-gray-900 mb-4">Contact Information</h3>
            <div class="space-y-4">
              <div class="flex items-center space-x-3">
                <svg class="w-5 h-5 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"/>
                </svg>
                <span class="text-gray-700 font-medium">(555) 123-4567</span>
              </div>
              <div class="flex items-center space-x-3">
                <svg class="w-5 h-5 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"/>
                </svg>
                <span class="text-gray-700">123 Fitness St, Gym City</span>
              </div>
              <div class="flex items-center space-x-3">
                <svg class="w-5 h-5 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
                  <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
                </svg>
                <span class="text-gray-700">info@fitlifegym.com</span>
              </div>
            </div>
          </div>
          
          <div class="space-y-4">
            <input
              v-model="contactForm.name"
              type="text"
              placeholder="Your Name"
              class="input-field"
            />
            <input
              v-model="contactForm.phone"
              type="tel"
              placeholder="Your Phone"
              class="input-field"
            />
            <textarea
              v-model="contactForm.message"
              placeholder="Your Message"
              rows="4"
              class="input-field resize-none"
            ></textarea>
            <button
              @click="sendContactMessage"
              class="btn-primary w-full"
            >
              Send Message
            </button>
            
            <p v-if="contactMessage" class="text-sm" :class="contactMessageClass">
              {{ contactMessage }}
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="py-20 bg-primary-600 text-white">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl md:text-4xl font-bold mb-6">
          Ready to Start Your Fitness Journey?
        </h2>
        <p class="text-xl text-primary-100 mb-8">
          Book your first training session today and take the first step towards a healthier, stronger you.
        </p>
        <router-link to="/book" class="btn-secondary text-lg px-8 py-4 inline-block bg-white text-primary-600 hover:bg-gray-100">
          Book Now
        </router-link>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      newsletterEmail: '',
      newsletterMessage: '',
      newsletterMessageClass: '',
      contactForm: {
        name: '',
        phone: '',
        message: ''
      },
      contactMessage: '',
      contactMessageClass: ''
    }
  },
  methods: {
    subscribeNewsletter() {
      if (!this.newsletterEmail) {
        this.newsletterMessage = 'Please enter your email address.';
        this.newsletterMessageClass = 'text-red-600';
        return;
      }
      
      if (!this.newsletterEmail.includes('@')) {
        this.newsletterMessage = 'Please enter a valid email address.';
        this.newsletterMessageClass = 'text-red-600';
        return;
      }
      
      this.newsletterMessage = 'Thank you for subscribing!';
      this.newsletterMessageClass = 'text-green-600';
      this.newsletterEmail = '';
      
      setTimeout(() => {
        this.newsletterMessage = '';
        this.newsletterMessageClass = '';
      }, 3000);
    },
    
    sendContactMessage() {
      if (!this.contactForm.name || !this.contactForm.phone || !this.contactForm.message) {
        this.contactMessage = 'Please fill in all fields.';
        this.contactMessageClass = 'text-red-600';
        return;
      }
      
      this.contactMessage = 'Thank you for your message! We\'ll get back to you soon.';
      this.contactMessageClass = 'text-green-600';
      
      this.contactForm = {
        name: '',
        phone: '',
        message: ''
      };
      
      setTimeout(() => {
        this.contactMessage = '';
        this.contactMessageClass = '';
      }, 3000);
    }
  }
}
</script>
