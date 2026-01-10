<script setup>
import { reactive } from 'vue'

const states = reactive([
  {
    img: '/imagess/logo5.png',
    title: 'Crafty-Bay',
    subtitle:
      'Developed using: Flutter, GetX State Management, REST API, MVVM architecture, & SSLCOMMERZ Payment Gateway || Users can add their desired products to the wish list or cart list here.',
    playstore: '',
    driveLink: 'https://drive.google.com/file/d/1zOWDuW0mN797JX7gL4womPk64ZygrTxe/view?usp=sharing',
    appstore: '', // yes
    github: 'https://github.com/iamsohan100/E-Commerce-Project',
  },
  {
    img: '/imagess/logo1.png',
    title: 'World-Vision',
    subtitle:
      'Developed using: Flutter, GetX State Management, REST API, MVC architecture || Before applying, the user must first login and then submit all the required information information information.',
    playstore: '', // no
    driveLink: 'https://drive.google.com/file/d/1qb2sz1meoZHUSoFUE4GXnPvfq50zyTP-/view?usp=sharing',
    appstore: '',
    github: 'https://github.com/iamsohan100/World-Vision',
  },
])

// Playstore
function openPlaystore(project) {
  if (project.playstore) {
    window.open(project.playstore, '_blank', 'noopener')
  } else if (project.driveLink) {
    window.open(project.driveLink, '_blank', 'noopener')
  } else {
    alert('iamsohan11@gmail.com')
  }
}

// Appstore
function openAppstore(project) {
  if (project.appstore) {
    window.open(project.appstore, '_blank', 'noopener')
  } else {
    alert('App Store link is currently unavailable !')
  }
}

// Init AOS
</script>

<template>
  <section id="project">
    <section class="py-8 items-center">
      <section class="text-center">
        <h1 class="lg:text-2xl xs:text-xl font-bold font-serif lg:mt-4 xs:-mt-4">
          <span class="text-cyan-400">My Projects</span>
        </h1>
        <div class="w-20 lg:h-1 xs:h-0.5 bg-blue-500 dark:bg-cyan-400 mx-auto mt-3 rounded"></div>
      </section>

      <div class="flex lg:mt-0.5 md:-mt-4">
        <section
          class="grid grid-cols-1 md:grid-cols-2 xs:mx-3 md:mx-auto lg:items-center lg:justify-center lg:flex md:gap-4 lg:gap-6 xs:p- md:p-10"
        >
          <div
            v-for="state in states"
            :key="state.title"
            class="group bg-gray-700 border-2 border-cyan-400 lg:h-[470px] lg:w-[370px] xs:w-full md:w-[320px] lg:mx-auto md:h-[432px] rounded-lg shadow-sm dark:bg-gray-800 relative overflow-hidden transform transition-all duration-500 hover:-translate-y-2 xs:mt-7 md:mt-4"
          >
            <div class="overflow-hidden lg:h-[230px]">
              <img
                class="w-full lg:h-full xs:h-[190px] md:h-[195px] object-cover transition-transform duration-500 group-hover:scale-110 group-hover:-translate-y-2"
                :src="state.img"
                alt=""
              />
            </div>

            <div class="lg:p-3 xs:p-2 xs:-mt-3 md:mt-">
              <h5 class="mb-2 text-2xl lg:mt- xs:mt-4 font-bold tracking-tight text-cyan-400">
                {{ state.title }}
              </h5>
              <p class="mb-3 text-cyan-400 text-base">
                {{ state.subtitle }}
              </p>

              <!-- Buttons -->
              <div class="flex items-center justify-between -mt-3">
                <div class="flex items-center gap-2">
                  <!-- Playstore -->
                  <button type="button" @click="openPlaystore(state)">
                    <!-- Playstore SVG -->
                    <svg
                      height="60px"
                      width="60px"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="-491.52 -491.52 1495.04 1495.04"
                      fill="currentColor"
                    >
                      <g>
                        <path
                          style="fill: #32bbff"
                          d="M382.369,175.623C322.891,142.356,227.427,88.937,79.355,6.028 C69.372-0.565,57.886-1.429,47.962,1.93l254.05,254.05L382.369,175.623z"
                        ></path>
                        <path
                          style="fill: #32bbff"
                          d="M47.962,1.93c-1.86,0.63-3.67,1.39-5.401,2.308C31.602,10.166,23.549,21.573,23.549,36v439.96 c0,14.427,8.052,25.834,19.012,31.761c1.728,0.917,3.537,1.68,5.395,2.314L302.012,255.98L47.962,1.93z"
                        ></path>
                        <path
                          style="fill: #32bbff"
                          d="M302.012,255.98L47.956,510.035c9.927,3.384,21.413,2.586,31.399-4.103 c143.598-80.41,237.986-133.196,298.152-166.746c1.675-0.941,3.316-1.861,4.938-2.772L302.012,255.98z"
                        ></path>
                      </g>
                      <path
                        style="fill: #2c9fd9"
                        d="M23.549,255.98v219.98c0,14.427,8.052,25.834,19.012,31.761c1.728,0.917,3.537,1.68,5.395,2.314 L302.012,255.98H23.549z"
                      ></path>
                      <path
                        style="fill: #29cc5e"
                        d="M79.355,6.028C67.5-1.8,53.52-1.577,42.561,4.239l255.595,255.596l84.212-84.212 C322.891,142.356,227.427,88.937,79.355,6.028z"
                      ></path>
                      <path
                        style="fill: #d93f21"
                        d="M298.158,252.126L42.561,507.721c10.96,5.815,24.939,6.151,36.794-1.789 c143.598-80.41,237.986-133.196,298.152-166.746c1.675-0.941,3.316-1.861,4.938-2.772L298.158,252.126z"
                      ></path>
                      <path
                        style="fill: #ffd500"
                        d="M488.45,255.98c0-12.19-6.151-24.492-18.342-31.314c0,0-22.799-12.721-92.682-51.809l-83.123,83.123 l83.204,83.205c69.116-38.807,92.6-51.892,92.6-51.892C482.299,280.472,488.45,268.17,488.45,255.98z"
                      ></path>
                      <path
                        style="fill: #ffaa00"
                        d="M470.108,287.294c12.191-6.822,18.342-19.124,18.342-31.314H294.303l83.204,83.205 C446.624,300.379,470.108,287.294,470.108,287.294z"
                      ></path>
                    </svg>
                  </button>

                  <!-- Appstore -->
                  <button type="button" @click="openAppstore(state)">
                    <!-- Appstore SVG -->
                    <svg
                      width="60px"
                      height="60px"
                      viewBox="-15.12 -15.12 54.24 54.24"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                      <g
                        id="SVGRepo_tracerCarrier"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                      ></g>
                      <g id="SVGRepo_iconCarrier">
                        <path
                          fill-rule="evenodd"
                          clip-rule="evenodd"
                          d="M15.2527 1.43981C14.3051 0.892747 13.1841 0.920762 12.2926 1.41459C11.3986 0.91084 10.2692 0.878945 9.3162 1.42916C7.88045 2.25809 7.38889 4.09421 8.21845 5.52961L8.83637 6.5988L5.75883 12H4C2.34315 12 1 13.3431 1 15C1 16.1186 1.61227 17.0943 2.51997 17.6101C1.75806 19.0253 2.25148 20.8071 3.6609 21.6208C5.07093 22.4349 6.87304 21.9733 7.71807 20.5816L9.2856 18H15.4166L16.8523 20.4866C17.681 21.9219 19.5163 22.4137 20.9516 21.585C22.5191 20.68 22.7936 18.7736 21.9374 17.2906C22.5874 16.7403 23 15.9184 23 15C23 13.3432 21.6569 12 20 12H18.8829L15.7588 6.58902L16.3635 5.52315C17.1776 4.08798 16.6816 2.26481 15.2527 1.43981ZM9.95006 4.52885C9.67338 4.0501 9.83733 3.43769 10.3162 3.16121C10.7389 2.91717 11.3548 3.01596 11.625 3.44531L12.285 4.58613L12.8787 3.5442C13.1543 3.06062 13.7707 2.89357 14.2527 3.17186C14.7302 3.44754 14.8959 4.05677 14.6239 4.53635L9.42464 13.7019C9.34908 13.8351 9.44513 14.0003 9.59826 14.0006L11.5527 14.0039C12.4981 14.0516 13.4113 14.5609 13.9035 15.3738C14.0822 15.6689 13.8666 16 13.5216 16L4 15.9999C3.45622 16 3 15.4858 3 15C3 14.4477 3.44772 14 4 14H6.80489C6.87675 14 6.94309 13.9614 6.97867 13.899L11.1382 6.5988L9.95006 4.52885ZM15.945 14.9151C15.8148 14.6313 15.6589 14.3621 15.4804 14.1105L14.3846 12.2124C13.7811 11.1672 13.8781 9.90983 14.5298 8.98378C14.6093 8.87095 14.7756 8.88594 14.8446 9.00542L17.6705 13.9C17.7062 13.9619 17.7722 14 17.8437 14H20C20.5523 14 21 14.4478 21 15C21 15.5 20.5 16 20 16H19.3324C19.1817 16 19.0851 16.1605 19.1557 16.2937L20.318 18.4857C20.5944 18.9644 20.4304 19.5766 19.9516 19.853C19.4729 20.1294 18.8607 19.9653 18.5843 19.4866L15.945 14.9151ZM4.56224 18.0956C4.59859 18.0362 4.6632 18 4.73283 18H6.59036C6.74629 18 6.84225 18.1705 6.76132 18.3038L6.00854 19.5436C5.72785 20.0058 5.12926 20.1592 4.6609 19.8888C4.17647 19.6091 4.01782 18.9851 4.30983 18.508L4.56224 18.0956Z"
                          fill="#ffffff"
                        ></path>
                      </g>
                    </svg>
                  </button>
                </div>

                <!-- Github -->

                <a v-if="state.github" :href="state.github" target="_blank">
                  <button
                    class="py-2 px-5 lg:-mt-3 text-sm font-medium text-black bg-cyan-400 border border-cyan-400 rounded-lg shadow-md hover:bg-[#1f242d] hover:text-white transition"
                  >
                    GitHub
                  </button>
                </a>
              </div>
            </div>
          </div>
        </section>
      </div>
    </section>
  </section>
</template>
