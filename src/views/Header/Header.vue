<script setup>
import { ref, onMounted } from 'vue'

const isOpen = ref(false)
const isDark = ref(false)

const toggleMenu = () => {
  isOpen.value = !isOpen.value
}

const closeMenu = () => {
  isOpen.value = false
}

const handleLinkClick = () => {
  closeMenu()
  setTimeout(() => {
    const hash = window.location.hash
    if (hash) {
      const target = document.querySelector(hash)
      if (target) {
        target.scrollIntoView({ behavior: 'smooth' })
      }
    }
  }, 100)
}

// const toggleDarkMode = () => {
//   isDark.value = !isDark.value
//   if (isDark.value) {
//     document.documentElement.classList.add('dark')
//     localStorage.setItem('theme', 'dark')
//   } else {
//     document.documentElement.classList.remove('dark')
//     localStorage.setItem('theme', 'light')
//   }
// }

onMounted(() => {
  const theme = localStorage.getItem('theme')
  if (theme === 'dark') {
    isDark.value = true
    document.documentElement.classList.add('dark')
  }
})
</script>

<template>
  <nav class="fixed top-0 left-0 w-full z-50 opacity-95 bg-[#1f242d] backdrop-blur-md shadow-md">
    <div class="max-w-7xl mx-auto flex items-center justify-between p-3.5">
      <!-- Logo -->
      <div class="lg:text-2xl font-bold text-white font-serif">
        Portfolio<span class="text-cyan-500">.</span>
      </div>

      <!-- Desktop Menu -->
      <ul class="hidden md:flex items-center space-x-8 font-bold font-serif text-[16px] text-white">
        <li>
          <a href="#home" @click="handleLinkClick" class="transition underline text-cyan-400"
            >Home</a
          >
        </li>
        <li>
          <a href="#experiance" @click="handleLinkClick" class="hover:text-cyan-400 hover:underline"
            >Experiance</a
          >
        </li>
        <li>
          <a href="#skill" @click="handleLinkClick" class="hover:text-cyan-400 hover:underline"
            >Skills</a
          >
        </li>
        <li>
          <a href="#project" @click="handleLinkClick" class="hover:text-cyan-400 hover:underline"
            >Projects</a
          >
        </li>
        <li>
          <a
            href="#cirtificate"
            @click="handleLinkClick"
            class="hover:text-cyan-400 hover:underline"
            >Cirtificate</a
          >
        </li>
        <li>
          <a href="#education" @click="handleLinkClick" class="hover:text-cyan-400 hover:underline"
            >Education</a
          >
        </li>
        <li>
          <a href="#contact" @click="handleLinkClick" class="hover:text-cyan-400 hover:underline"
            >Contact</a
          >
        </li>
        <li>
          <!-- <button @click="toggleDarkMode" class="text-2xl ml-3">
            <span v-if="!isDark">🌙</span>
            <span v-else>☀️</span>
          </button> -->
        </li>
      </ul>

      <!-- Mobile Menu Button -->
      <div class="md:hidden flex items-center space-x-4">
        <!-- <button @click="toggleDarkMode" class="text-2xl text-gray-800 dark:text-white">
          <span v-if="!isDark">🌙</span>
          <span v-else>☀️</span>
        </button> -->
        <button @click="toggleMenu" class="text-gray-800 dark:text-white">
          <svg v-if="!isOpen" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
          </svg>
          <svg v-else class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>
    </div>

    <!-- Mobile Menu Items -->
    <transition name="slide-fade">
      <div
        v-if="isOpen"
        class="md:hidden flex flex-col space-y-4 px-6 pb-6 pt-2 bg-gray-100 dark:bg-[#1e293b]/90 backdrop-blur-md shadow-sm border-t text-gray-800 dark:text-gray-100 font-serif font-semibold text-base"
      >
        <a href="#home" @click="handleLinkClick" class="hover:text-cyan-500">Home</a>
        <a href="#experiance" @click="handleLinkClick" class="hover:text-cyan-500">Experiance</a>
        <a href="#skill" @click="handleLinkClick" class="hover:text-cyan-500">Skills</a>
        <a href="#project" @click="handleLinkClick" class="hover:text-cyan-500">Projects</a>
        <a href="#cirtificate" @click="handleLinkClick" class="hover:text-cyan-500">Cirtificate</a>
        <a href="#education" @click="handleLinkClick" class="hover:text-cyan-500">Education</a>
        <a href="#contact" @click="handleLinkClick" class="hover:text-cyan-500">Contact</a>
      </div>
    </transition>
  </nav>
</template>

<style scoped>
.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: all 0.3s ease;
}
.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateY(-10px);
  opacity: 0;
}
</style>
