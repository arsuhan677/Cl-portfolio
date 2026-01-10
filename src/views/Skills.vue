<script setup>
import { reactive, ref, computed } from 'vue'

const filterType = ref('all') // all, group2, group3

const states = reactive([
  // Group 1
  { img: '/images/dart.png', title: 'dart', subtitle1: 'Modern OOP language', group: 'group1' },
  {
    img: '/images/flutter.png',
    title: 'flutter',
    subtitle1: 'UI toolkit for cross-platform apps',
    group: 'group1',
  },
  {
    img: '/images/java.png',
    title: 'java',
    subtitle1: 'used language for backend',
    group: 'group1',
  },
  {
    img: '/images/getx.png',
    title: 'getx',
    subtitle1: 'Lightweight state management',
    group: 'group1',
  },
  {
    img: '/images/jj.png',
    title: 'provider',
    subtitle1: 'Scalable state management library',
    group: 'group1',
  },
  {
    img: '/images/restapi.png',
    title: 'Rest api',
    subtitle1: 'Standard client-server communication',
    group: 'group1',
  },
  {
    img: '/images/mvvc.png',
    title: 'mvvm',
    subtitle1: 'Clean separation of UI, logic & data',
    group: 'group1',
  },
  {
    img: '/images/mvc.png',
    title: 'mvc',
    subtitle1: 'Model, View & Controller pattern',
    group: 'group1',
  },

  // Group 2
  {
    img: '/images/oop.png',
    title: 'oop',
    subtitle1: 'Modular, reusable coding approach',
    group: 'group2',
  },
  {
    img: '/images/firebase.png',
    title: 'firebase',
    subtitle1: 'Auth, DB, Hosting',
    group: 'group2',
  },
  {
    img: '/images/admod.png',
    title: 'AdMob',
    subtitle1: 'Mobile app monetization tool',
    group: 'group2',
  },
  {
    img: '/images/map.png',
    title: 'google map',
    subtitle1: 'Location & navigation API',
    group: 'group2',
  },
  {
    img: '/images/eps.png',
    title: 'eps',
    subtitle1: 'Secure electronic payment system',
    group: 'group2',
  },
  {
    img: '/images/SSLCOMMERZ.png',
    title: 'SSLCOMMERZ',
    subtitle1: 'Leading BD online payment gateway',
    group: 'group2',
  },

  // Group 3
  { img: '/images/git.png', title: 'git', subtitle1: 'Version control system', group: 'group3' },
  {
    img: '/images/github.png',
    title: 'github',
    subtitle1: 'Cloud Git repository platform',
    group: 'group3',
  },
  {
    img: '/images/figma.png',
    title: 'figma',
    subtitle1: 'Collaborative UI/UX design tool',
    group: 'group3',
  },
  {
    img: '/images/jira.png',
    title: 'jira',
    subtitle1: 'Agile project management tool',
    group: 'group3',
  },
  {
    img: '/images/postman.png',
    title: 'postman',
    subtitle1: 'API testing & development tool',
    group: 'group3',
  },
  {
    img: '/images/trello.png',
    title: 'trello',
    subtitle1: 'Visual project management board',
    group: 'group3',
  },
])

// Filter
const filteredStates = computed(() => {
  if (filterType.value === 'all') return states
  return states.filter((item) => item.group === filterType.value)
})
</script>

<template>
  <section id="skill">
    <section class="py-8 items-center">
      <section class="text-center">
        <h1 class="lg:text-2xl xs:text-xl font-serif font-bold xs:mt-2 md:mt-2 lg:-mt-5">
          <span class="text-cyan-400">My Skills</span>
        </h1>
        <p class="mt-2 text-white">Technologies I work with</p>
        <div class="w-20 lg:h-1 xs:h-0.5 bg-cyan-500 mx-auto mt-3 rounded"></div>
      </section>

      <!-- Filter Buttons -->
      <div class="flex justify-center gap-4 mt-6">
        <button
          @click="filterType = 'all'"
          :class="[
            'px-6 py-2 rounded-full text-sm font-medium',
            filterType === 'all'
              ? 'bg-cyan-400 text-black'
              : 'bg-gray-800 text-white hover:bg-cyan-600',
          ]"
        >
          All
        </button>
        <button
          @click="filterType = 'group2'"
          :class="[
            'px-4 py-2 rounded-full text-sm font-medium',
            filterType === 'group2'
              ? 'bg-cyan-400 text-black'
              : 'bg-gray-800 text-white hover:bg-cyan-600',
          ]"
        >
          Familiar
        </button>
        <button
          @click="filterType = 'group3'"
          :class="[
            'px-4 py-2 rounded-full text-sm font-medium',
            filterType === 'group3'
              ? 'bg-cyan-400 text-black'
              : 'bg-gray-800 text-white hover:bg-cyan-600',
          ]"
        >
          Comfortable
        </button>
      </div>

      <section
        class="xs:mx-0.5 w-full xs:mt-8 lg:mt-16 px-3 md:px-12 lg:px-24 grid lg:gap-4 md:gap-4 xs:gap-2 xs:grid-cols-2 md:grid-cols-4 lg:grid-cols-5"
      >
        <div
          data-aos="fade-up"
          data-aos-anchor-placement="top-bottom"
          data-aos-duration="1000"
          v-for="(state, index) in filteredStates"
          :key="index"
          class="w-full h-auto xs:h-[144px] md:h-[160px] p-3 rounded-lg bg-gray-900 dark:border-gray-700 transition-transform duration-500 xs:border lg:dark:border-2 border-cyan-700 hover:border-2 hover:border-cyan-400 hover:scale-[1.03] lg:h-[180px] xs:p-3 md:p-5 hover:shadow-lg shadow"
        >
          <div
            class="bg-gray-300 p-3 rounded-full flex text-blue-600 lg:w-14 lg:h-14 xs:w-11 xs:h-11 justify-center items-center"
          >
            <img class="lg:w-[30px] lg:h-[30px] xs:w-[26px] xs:h-[18px]" :src="state.img" alt="" />
          </div>
          <div>
            <h1
              class="xs:text-[13.5px] lg:text-base md:text- text-cyan-400 uppercase font-bold lg:mt-3 md:mt-2 xs:mt-3"
            >
              {{ state.title }}
            </h1>
            <p
              class="lg:text-sm xs:text-[12px] mb-3 xs:mt-1 lg:mt-2 font-normal text-white dark:text-cyan-300"
            >
              {{ state.subtitle1 }}
            </p>
          </div>
        </div>
      </section>
    </section>
  </section>
</template>
