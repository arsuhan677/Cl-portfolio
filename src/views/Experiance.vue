<script setup>
import { ref } from 'vue';

// ref
const showMore = ref(false); 
</script>

<template>
<div>
hello div
</div>

    <section id="experiance" class="lg:py-24">
  <div class="containe xs:-mx-1 lg:mx-12 px-5 md:px-12 lg:px-16 flex flex-col lg:flex-row items-center lg:items-start lg:mt-14">

    <div data-aos="zoom-in"
    data-aos-duration="3000"
     class="lg:w-1/2 flex justify-center lg:justify-start xs:mt-12 md:-mt-20 mx-auto duration-500 transition hover:scale-[1.03]">
      <img
        src="/images/sohan.png"
        alt="About Image"
        class="xs:w-[230px] xs:h-[240px] sm:w-[280px] sm:h-[260px] md:w-[280px] md:h-[280px] lg:w-[280px] lg:h-[320px] lg:mt-4 rounded-xl border-2 border-cyan-400 object-cover shadow-[0_0_25px_rgba(0,0.2)] shadow-cyan-400 duration-500 transition"
      />
    </div>


    <div class="lg:-mt-20 w-full text-black md:mt-10 xs:mt-10">
      <h1 data-aos="fade-left"
              data-aos-offset="50"
              data-aos-easing="ease-in-sine"
              data-aos-duration="1250"
              class="lg:text-2xl xs:text-xl sm:text-xl font-bold font-serif mb-4 text-center lg:text-left">
        <span class=" text-cyan-400">Job Experiance</span>
      </h1>

      <!-- -->

      <ul class="mt-6 space-y-2 text-xs sm:text-base text-white xs:text-[14px] md:text-[16px] lg:text-[18px] xs:-mx-1">
        <li data-aos="fade-left"
              data-aos-offset="50"
              data-aos-easing="ease-in-sine"
              data-aos-duration="1200" class="flex md:justify-center lg:justify-start">
          <span class="text-cyan-400 mr-2">📅 11/2024 - Present</span>
        </li>
        <li data-aos="fade-left"
              data-aos-offset="50"
              data-aos-easing="ease-in-sine"
              data-aos-duration="1150" class="flex md:justify-center lg:justify-start">
          <span class="text-base text-center font-semibold lg:text-left text-white mb-2 lg:text-xl lg:mt-1">Junior Software Enginner (Flutter)</span>
        </li>
        <li data-aos="fade-left"
              data-aos-offset="50"
              data-aos-easing="ease-in-sine"
              data-aos-duration="1100" class="flex md:justify-center lg:justify-start">
          <span class="text-base text-center font-semibold lg:text-left text-white mb-2 lg:text-xl xs:text-[17px] lg:mt-1">Code Studio - </span>
          <a href="https://code-studio4.com/"><span class="text-base text-center font-semibold lg:text-left text-cyan-400 mb-2 lg:text-xl xs:text-[17px] lg:mt-1 hover:underline">🔗 www.code-studio4.com</span></a>
        </li>
      </ul>

      <p data-aos="fade-left"
              data-aos-offset="50"
              data-aos-easing="ease-in-sine"
              data-aos-duration="1050" class="text-white mb-6 xs:mt-3 xs:text-[14px] lg:text-[18px] md:text-[16px] xs:-mx-1 md:text-center lg:text-start">
          Worked closely with clients to understand their needs, ensuring that each project met their specific
          requirements and goals.
      </p>
      <!-- ... -->
      <div>

      </div>

      <div data-aos="fade-left"
              data-aos-offset="50"
              data-aos-easing="ease-in-sine"
              data-aos-duration="1200" class="flex flex-col gap-4 w-full md:w-auto items-center lg:items-start mt-4 md:items-center md:flex md:justify-center md:mt-8">
         <div>
    <p>
    </p>

    <div v-if="showMore">
      <div>
        <div>
        <p class="text-base text-center font-semibold lg:text-left text-white mb-2 lg:text-xl lg:-mt-3">
        Key Learnings & Contributions:
      </p>
      </div>
        <div>
        <li class="text-white xs:mt-3 xs:text-sm lg:text-[18px] md:text-base xs:mx-4 md:text-start lg:text-start">
          <span class="mr-2">
          Implemented MVVM architecture for scalable and maintainable code.</span>
        </li>
        <li class="text-white xs:mt-3 xs:text-[14px] lg:text-[18px] md:text-[16px] xs:mx-4 md:text-start lg:text-start">
          <span class="mr-2">
           Applied Provider and GetX for state management in different projects.</span>
        </li>
        <li class="text-white xs:mt-3 xs:text-[14px] lg:text-[18px] md:text-[16px] xs:mx-4 md:text-start lg:text-start">
          <span class="mr-2">
           Integrated GoRouter for smooth navigation and route handling.</span>
        </li>
        <li class="text-white xs:mt-3 xs:text-[14px] lg:text-[18px] md:text-[16px] xs:mx-4 md:text-start lg:text-start">
          <span class="mr-2">
           Worked on Push Notification implementation using Firebase Messaging.</span>
        </li>
        <li class="text-white xs:mt-3 xs:text-[14px] lg:text-[18px] md:text-[16px] xs:mx-4 md:text-start lg:text-start">
          <span class="mr-2">
           Integrated Google Maps API for location-based features.</span>
        </li>
        <li class="text-white xs:mt-3 xs:text-[14px] lg:text-[18px] md:text-[16px] xs:mx-4 md:text-start lg:text-start">
          <span class="mr-2">
           Practiced effective team communication & collaboration in remote projects.</span>
        </li>
        <li class="text-white xs:mt-3 xs:text-[14px] lg:text-[18px] md:text-[16px] xs:mx-4 md:text-start lg:text-start">
          <span class="mr-2">
          Improved debugging and problem-solving skills while working on real client projects</span>
        </li>
      </div>
      </div>
    </div>

    <div class="md:items-center md:flex md:justify-center lg:items-start lg:justify-start xs:items-center xs:flex xs:justify-center">
      <button class="xs:w-48 md:w-52 lg:w-29 lg:py-2 md:px-4 shadow-[#00f0ff] xs:py-2 md:py-3 mt-2 text-black bg-[#00f0ff] hover:bg-cyan-500 shadow-[0_0_5px_rgba(0,0,0,0.4)] rounded-full font-medium transition duration-500 hover:shadow-[#00f0ff] xs:text-sm lg:text-lg" 
      @click="showMore = !showMore">
      {{ showMore ? 'Show Less' : 'Read More' }}
    </button>
    </div>
  </div>
        </div>
    </div>
  </div>
</section>
</template>

<style scoped>
</style>