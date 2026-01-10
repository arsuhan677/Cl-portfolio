<script setup>
import { ref } from 'vue'

const showMore = ref(false)
</script>

<template>
  <section id="experience" class="py-16">
    <div class="max-w-6xl mx-auto">
      <h1 class="text-2xl font-bold text-center mb-10">
        <span class="text-cyan-400">Job Experience</span>
      </h1>

      <!-- Cards -->
      <div class="flex flex-col lg:flex-row gap-8">
        <!-- Card 1 -->
        <div
          class="relative flex-1 bg-[#1f2937] rounded-xl p-6 pt-14 border border-cyan-400 shadow-[0_0_20px_rgba(0,255,255,0.2)]"
        >
          <!-- Logo -->
          <div
            class="absolute -top-7 left-1/2 -translate-x-1/2 w-14 h-14 bg-cyan-400 rounded-full flex items-center justify-center text-black text-2xl shadow-lg"
          >
            💼
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
            <p class="text-gray-300 text-sm md:text-base text-center lg:text-left">
              Worked closely with clients to understand their needs, ensuring that each project met
              their specific requirements and goals.
            </p>
            <ul class="space-y-2 text-gray-300 text-sm md:text-base">
            <li>✔ Implemented MVVM architecture for scalable Flutter applications</li>
            <li class="case-in-1">✔ Used Provider and GetX for state management across multiple projects</li>
            <li>✔ Integrated Firebase Cloud Messaging for push notifications</li>
            <li>✔ Implemented Google Maps API for location-based features</li>
            <li>✔ Collaborated with remote team members and improved debugging skills</li>
          </ul>
          </div>
        </div>

        <!-- Card 2 -->
        <div
          class="relative flex-1 bg-[#1f2937] rounded-xl p-6 pt-14 border border-cyan-400 shadow-[0_0_20px_rgba(0,255,255,0.2)]"
        >
          <!-- Logo -->
          <div
            class="absolute -top-7 left-1/2 -translate-x-1/2 w-14 h-14 bg-cyan-400 rounded-full flex items-center justify-center text-black text-2xl shadow-lg"
          >
            💼
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
              www.code-studio4.com
            </a>
          </p>

          <div class="space-y-4">
            <p class="text-gray-300 text-sm md:text-base text-center lg:text-left">
              Worked closely with clients to understand their needs, ensuring that each project met
              their specific requirements and goals.
            </p>
            <ul class="space-y-2 text-gray-300 text-sm md:text-base">
            <li>✔ Implemented MVVM architecture for scalable Flutter applications</li>
            <li class="case-in-1">✔ Used Provider and GetX for state management across multiple projects</li>
            <li>✔ Integrated Firebase Cloud Messaging for push notifications</li>
            <li>✔ Implemented Google Maps API for location-based features</li>
            <li>✔ Collaborated with remote team members and improved debugging skills</li>
          </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
