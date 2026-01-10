<script setup>
import { ref } from 'vue'

const certificates = [
  '/imagess/cirtificate1.jpg', // 1st
  '/imagess/marksheet.jpg', // 2nd
]

const currentIndex = ref(0)

const prevCertificate = () => {
  currentIndex.value = 0
}

const nextCertificate = () => {
  currentIndex.value = 1
}
</script>

<template>
  <div id="cirtificate" class="flex-col items-center py-10 px-5">
    <!-- Heading -->
    <section class="text-center">
      <h1 class="lg:text-2xl xs:text-xl font-serif font-bold xs:-mt-6 lg:mt-1">
        <span class="text-cyan-400">Certificate of Achievement</span>
      </h1>
      <p class="mt-2 lg:text-[16px] text-white">
        Complete App Development With Flutter Ostad, Flutter Batch-4
      </p>
      <div class="w-20 lg:h-1 xs:h-0.5 bg-cyan-400 mx-auto mt-3 rounded"></div>
    </section>

    <!-- Buttons -->
    <div class="flex gap-4 mt-12 justify-center">
      <button
        @click="prevCertificate"
        :class="[
          'px-6 py-2 rounded-full shadow transition',
          currentIndex === 0 ? 'bg-cyan-400 text-white' : 'bg-white text-black',
        ]"
      >
        Cirtificate
      </button>
      <button
        @click="nextCertificate"
        :class="[
          'px-6 py-2 rounded-full shadow transition',
          currentIndex === 1 ? 'bg-cyan-400 text-white' : 'bg-white text-black',
        ]"
      >
        Marksheet
      </button>
    </div>

    <!-- Certificate Image -->
    <div
      data-aos="fade-zoom-in"
      data-aos-easing="ease-in-back"
      data-aos-delay="100"
      data-aos-offset="0"
      class="flex justify-center mt-11 xs:-mx-1.5 h-auto"
    >
      <img
        :src="certificates[currentIndex]"
        alt="Certificate"
        class="w-full max-w-3xl h-auto mx-6 border-2 border-gray-300 rounded-lg shadow-lg transition-transform duration-300 hover:scale-[1.01] hover:border-2 hover:border-cyan-400"
      />
    </div>
  </div>
</template>
