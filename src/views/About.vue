<template>
  <div class="min-h-screen bg-gray-50">
    <!-- Hero Section -->
    <section class="relative bg-gradient-to-br from-primary-600 via-primary-700 to-primary-800 text-white py-20 lg:py-32">
      <div class="absolute inset-0 bg-black bg-opacity-20"></div>
      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
          About FitLife Gym
        </h1>
        <p class="text-xl md:text-2xl mb-8 text-primary-100 max-w-3xl mx-auto">
          We're more than just a gym. We're a community dedicated to helping you achieve your fitness goals and transform your life.
        </p>
        
        <!-- Phone Number in Hero -->
        <div class="flex items-center justify-center space-x-2 mb-8 text-primary-100">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20">
            <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"/>
          </svg>
          <span class="text-2xl font-bold">(555) 123-4567</span>
        </div>
        
        <router-link to="/book" class="btn-primary text-lg px-8 py-4 inline-block">
          Book Your First Session
        </router-link>
      </div>
    </section>

    <!-- Our Story Section -->
    <section class="py-20 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          <div>
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-6">
              Our Story
            </h2>
            <p class="text-lg text-gray-600 mb-6">
              FitLife Gym was founded in 2010 with a simple mission: to make fitness accessible, enjoyable, and effective for everyone. What started as a small local gym has grown into a thriving fitness community that has helped thousands of people transform their lives.
            </p>
            <p class="text-lg text-gray-600 mb-6">
              We believe that fitness is not just about looking good – it's about feeling great, building confidence, and improving your overall quality of life. Our approach combines cutting-edge equipment, expert guidance, and a supportive community to help you reach your goals.
            </p>
            <p class="text-lg text-gray-600">
              Whether you're a complete beginner or a seasoned athlete, we have the resources, expertise, and motivation to help you succeed on your fitness journey.
            </p>
          </div>
          
          <div class="relative">
            <div class="bg-primary-100 rounded-2xl p-8 text-center">
              <div class="w-24 h-24 bg-primary-600 rounded-full flex items-center justify-center mx-auto mb-6">
                <svg class="w-12 h-12 text-white" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd"/>
                </svg>
              </div>
              <h3 class="text-2xl font-bold text-gray-900 mb-4">13+ Years of Excellence</h3>
              <p class="text-gray-600">
                Serving our community since 2010 with dedication, expertise, and a passion for fitness.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Our Mission Section -->
    <section class="py-20 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-6">
          Our Mission & Values
        </h2>
        <p class="text-xl text-gray-600 mb-12 max-w-3xl mx-auto">
          We're committed to creating an inclusive, supportive environment where everyone can achieve their fitness goals.
        </p>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="card text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Excellence</h3>
            <p class="text-gray-600">We strive for excellence in everything we do, from our equipment to our training programs.</p>
          </div>
          
          <div class="card text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Community</h3>
            <p class="text-gray-600">Building a supportive community where members motivate and inspire each other.</p>
          </div>
          
          <div class="card text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
                <svg class="w-8 h-8 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M11.3 1.046A1 1 0 0112 2v5h4a1 1 0 01.82 1.573l-7 10A1 1 0 018 18v-5H4a1 1 0 01-.82-1.573l7-10a1 1 0 011.12-.38z" clip-rule="evenodd"/>
                </svg>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Innovation</h3>
            <p class="text-gray-600">Continuously innovating our training methods and facilities to provide the best experience.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Our Trainers Section -->
    <section class="py-20 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            Meet Our Expert Trainers
          </h2>
          <p class="text-xl text-gray-600 max-w-2xl mx-auto">
            Our certified trainers bring years of experience and expertise to help you achieve your fitness goals.
          </p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div class="card text-center">
            <div class="w-32 h-32 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-6">
              <svg class="w-16 h-16 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Sarah Johnson</h3>
            <p class="text-primary-600 font-medium mb-2">Head Trainer & Nutritionist</p>
            <p class="text-gray-600 text-sm mb-4">
              Certified personal trainer with 8+ years of experience specializing in weight loss and nutrition coaching.
            </p>
            <p class="text-sm text-gray-500">
              NASM Certified, Precision Nutrition Coach
            </p>
          </div>
          
          <div class="card text-center">
            <div class="w-32 h-32 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-6">
              <svg class="w-16 h-16 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Mike Rodriguez</h3>
            <p class="text-primary-600 font-medium mb-2">Strength & Conditioning Specialist</p>
            <p class="text-gray-600 text-sm mb-4">
              Former collegiate athlete with expertise in strength training, HIIT, and sports performance.
            </p>
            <p class="text-sm text-gray-500">
              CSCS Certified, USA Weightlifting Coach
            </p>
          </div>
          
          <div class="card text-center">
            <div class="w-32 h-32 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-6">
              <svg class="w-16 h-16 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Emma Chen</h3>
            <p class="text-primary-600 font-medium mb-2">Yoga & Flexibility Expert</p>
            <p class="text-gray-600 text-sm mb-4">
              Certified yoga instructor specializing in flexibility, mobility, and stress relief through movement.
            </p>
            <p class="text-sm text-gray-500">
              RYT-200, Functional Movement Specialist
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Facilities Section -->
    <section class="py-20 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            State-of-the-Art Facilities
          </h2>
          <p class="text-xl text-gray-600 max-w-2xl mx-auto">
            Our modern facility is equipped with everything you need for an effective and enjoyable workout experience.
          </p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
          <div class="bg-white p-6 rounded-lg text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path d="M3 4a1 1 0 011-1h12a1 1 0 011 1v2a1 1 0 01-1 1H4a1 1 0 01-1-1V4zM3 10a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H4a1 1 0 01-1-1v-6zM14 9a1 1 0 00-1 1v6a1 1 0 001 1h2a1 1 0 001-1v-6a1 1 0 00-1-1h-2z"/>
              </svg>
            </div>
            <h3 class="font-semibold text-gray-900 mb-2">Cardio Zone</h3>
            <p class="text-sm text-gray-600">Treadmills, ellipticals, bikes, and rowing machines</p>
          </div>
          
          <div class="bg-white p-6 rounded-lg text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
            </div>
            <h3 class="font-semibold text-gray-900 mb-2">Strength Training</h3>
            <p class="text-sm text-gray-600">Free weights, machines, and functional training equipment</p>
          </div>
          
          <div class="bg-white p-6 rounded-lg text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="font-semibold text-gray-900 mb-2">Group Classes</h3>
            <p class="text-sm text-gray-600">HIIT, yoga, spinning, and specialized fitness classes</p>
          </div>
          
          <div class="bg-white p-6 rounded-lg text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-primary-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="font-semibold text-gray-900 mb-2">Recovery Zone</h3>
            <p class="text-sm text-gray-600">Sauna, steam room, and massage therapy</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact & CTA Section -->
    <section class="py-20 bg-primary-600 text-white">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl md:text-4xl font-bold mb-6">
          Ready to Start Your Fitness Journey?
        </h2>
        <p class="text-xl text-primary-100 mb-8">
          Join our community today and take the first step towards a healthier, stronger you. Our expert trainers are here to guide you every step of the way.
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center mb-8">
          <router-link to="/book" class="btn-secondary text-lg px-8 py-4 bg-white text-primary-600 hover:bg-gray-100">
            Book Your Session
          </router-link>
          <a href="tel:(555) 123-4567" class="btn-secondary text-lg px-8 py-4 border-2 border-white text-white hover:bg-white hover:text-primary-600">
            Call Us Now
          </a>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mt-12">
          <div class="text-center">
            <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"/>
              </svg>
            </div>
            <h3 class="text-lg font-semibold mb-2">Call Us</h3>
            <p class="text-primary-100">(555) 123-4567</p>
          </div>
          
          <div class="text-center">
            <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
                <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
              </svg>
            </div>
            <h3 class="text-lg font-semibold mb-2">Email Us</h3>
            <p class="text-primary-100">info@fitlifegym.com</p>
          </div>
          
          <div class="text-center">
            <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-lg font-semibold mb-2">Visit Us</h3>
            <p class="text-primary-100">123 Fitness St, Gym City</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'About'
}
</script>
