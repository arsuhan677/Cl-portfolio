<script setup>
import { ref } from 'vue'

const showMore = ref(false)
</script>

<template>
  <section id="experiance" class="py-16">
    <!-- Main Wrapper -->
    <div class="max-w-6xl mx-auto px-4">
      <h1 class="text-2xl font-bold text-center mb-10">
        <span class="text-cyan-400">Job Experience</span>
      </h1>

      <!-- Cards Wrapper -->
      <div class="flex flex-col lg:flex-row lg:gap-8 xs:gap-10">
        <!-- ================= Card 1 ================= -->
        <div
          class="relative flex-1 bg-[#1f2937] rounded-xl p-6 pt-14 border border-cyan-400 shadow-[0_0_20px_rgba(0,255,255,0.2)]"
        >
          <!-- Logo -->
          <div
            class="absolute -top-8 left-1/2 -translate-x-1/2 w-16 h-16 border border-cyan-400 rounded-full flex items-center justify-center shadow-lg p-1 bg-white"
          >
            <img
              src="/images/logo.png"
              alt="Company Logo"
              class="w-full h-full object-contain rounded-full"
            />
          </div>

          <p class="text-cyan-400 mb-2">📅 11/2024 - Present</p>

          <h2 class="text-xl font-semibold text-white mb-1 text-center lg:text-left">
            Junior Software Engineer (Flutter)
          </h2>

          <p class="text-white mb-3 text-center lg:text-left">
            Code Studio –
            <a
              href="https://code-studio4.com/"
              target="_blank"
              class="text-cyan-400 hover:underline"
            >
              www.code-studio4.com
            </a>
          </p>

          <div class="space-y-4">
            <p class="text-gray-300 text-sm md:text-base text-center lg:text-left font-bold">
              Worked closely with clients to understand their needs, ensuring that each project met
              their specific requirements and goals.
            </p>

            <ul class="space-y-2 text-gray-300 text-sm md:text-base list-disc lg:pl-5 xs:pl-3.5">
              <li>Implemented MVVM architecture for scalable Flutter applications</li>
              <li><span>Used Provider and GetX for state management across multiple projects</span></li>
              <li>Integrated Firebase Cloud Messaging for push notifications</li>
              <li>Implemented Google Maps API for location-based features</li>
              <li>Collaborated with remote team members and improved debugging skills</li>
            </ul>
          </div>
        </div>

        <!-- ================= Card 2 ================= -->
        <div
          class="relative flex-1 bg-[#1f2937] rounded-xl p-6 pt-14 border border-cyan-400 shadow-[0_0_20px_rgba(0,255,255,0.2)]"
        >
          <!-- Logo -->
          <div
            class="absolute -top-8 left-1/2 -translate-x-1/2 w-16 h-16 border border-cyan-400 rounded-full flex items-center justify-center shadow-lg p-1 bg-white"
          >
            <img
              src="/images/images.jpg"
              alt="Company Logo"
              class="w-full h-full object-contain rounded-full"
            />
          </div>

          <p class="text-cyan-400 mb-2">📅 10/2025 – Present</p>

          <h2 class="text-xl font-semibold text-white mb-1 text-center lg:text-left">
            Software Engineer (Flutter)
          </h2>

          <p class="text-white mb-3 text-center lg:text-left">
            Sparktech Agency –
            <a
              href="https://www.sparktech.agency/"
              target="_blank"
              class="text-cyan-400 hover:underline"
            >
              www.sparktech.agency
            </a>
          </p>

          <div class="space-y-4">
            <p class="text-gray-300 text-sm md:text-base text-center lg:text-left font-bold">
              Worked with international clients through Upwork and Fiverr to deliver high-quality
              Flutter applications.
            </p>

            <ul class="space-y-2 text-gray-300 text-sm md:text-base list-disc lg:pl-5 xs:pl-3.5">
              <li>Implemented real-time audio calls, video calls, and live streaming</li>
              <li>Integrated Socket-based real-time data synchronization</li>
              <li>Followed Clean Architecture for scalable applications</li>
              <li>Collaborated with large cross-functional agile teams</li>
              <li>Integrated AI APIs to enhance app features and UX</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
