<script setup>
// Web3Forms Dashboard
import { reactive, ref } from 'vue'
const WEB3FORMS_ACCESS_KEY = 'f5dcfd60-8200-4087-862d-8d457546b6ed'
const name = ref('')
const email = ref('')
const message = ref('')
const showSuccess = ref(false)

const submitForm = async () => {
  console.log('submit')
  alert('Do you want to send the message?')
  const response = await fetch('https://api.web3forms.com/submit', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
      Accept: 'application/json',
    },
    body: JSON.stringify({
      access_key: WEB3FORMS_ACCESS_KEY,
      name: name.value,
      email: email.value,
      message: message.value,
    }),
  })

  const result = await response.json()
  if (result.success) {
    console.log(result)
    showSuccess.value = true //
    setTimeout(() => {
      showSuccess.value = false
    }, 1)
  }

  // input
  name.value = ''
  email.value = ''
  message.value = ''
}
</script>

<template>
  <section id="contact" class="">
    <section class="py-12 -my-1 shadow-lg dark:text-white">
      <section class="text-center">
        <h1 class="lg:text-2xl xs:text-xl font-serif font-bold md:-mt-10 lg:-mt-5 xs:-mt-10">
          <span class="text-cyan-400">Get In Touch</span>
        </h1>
        <p class="mt-2 lg:text-[16px] text-white">Let's work together</p>
        <div class="w-20 lg:h-1 xs:h-0.5 bg-cyan-400 mx-auto mt-3 rounded"></div>
      </section>

      <section
        data-aos="fade-up"
        data-aos-duration="1000"
        data-aos-anchor-placement="center-bottom"
        class="p-10 md:px-16 lg:mt-8 xs:py-10"
      >
        <div class="max-w-7xl mx-auto grid md:grid-cols-2 md:gap-20 lg:gap-24 xs:gap-6">
          <div class="xs:-mx-8 lg:h-[550px] lg:mt-6">
            <div class="space-x-2 mt-2 md:mt-16">
              <h2
                class="lg:text-3xl xs:text-xl xs:mx-1 lg:items-start lg:justify-start font-bold mb-4 lg:mx-6 text-white xs:-mt-6 md:justify-start"
              >
                Contact Information
              </h2>
              <p class="lg:text-[18px] xs:text-[14px] text-white mb-6 xs:-mt-1 lg:-mt-4 lg:p-6">
                I’m always open to job opportunities, collaborations, or conversations. If you have
                an idea or just want to say hello, feel free to reach out!
              </p>
              <div class="lg:space-y-10 xs:space-y-6">
                <div class="flex items-start -mt-2 lg:mx-4 lg:-mt-4 xs:-mx-4">
                  <div class="p-3 lg:rounded-sm xs:rounded-xl text-white mt-1.5">
                    <svg
                      class="lg:w-10 lg:h-10 md:w-10 md:h-10 xs:w-8 xs:h-8"
                      fill="currentColor"
                      viewBox="0 0 24 24"
                    >
                      <path d="M4 4h16v16H4z" fill="none" />
                      <path d="M20 4H4v16h16V4zM5.5 6.5l6.5 4.5 6.5-4.5V18H5.5V6.5z" />
                    </svg>
                  </div>
                  <div class="xs:-mt- lg:mx-2">
                    <h4 class="font-bold mt-3 mx-2 text-cyan-400">Email</h4>
                    <p class="text-white mx-2">iamsohan11@gmail.com</p>
                  </div>
                </div>
                <div class="flex items-start lg:mx-6 xs:-mx-4">
                  <div class="p-3 lg:rounded-sm xs:rounded-xl text-white lg:-mt-2 xs:-mt-1.5">
                    <svg
                      class="lg:w-10 lg:h-10 md:w-10 md:h-10 xs:w-8 xs:h-8"
                      fill="currentColor"
                      viewBox="0 0 24 24"
                    >
                      <path
                        d="M6.62 10.79a15.05 15.05 0 006.59 6.59l2.2-2.2a1 1 0 011.11-.27 11.72 11.72 0 003.69.59 1 1 0 011 1V20a1 1 0 01-1 1A16 16 0 014 5a1 1 0 011-1h3.5a1 1 0 011 1 11.72 11.72 0 00.59 3.69 1 1 0 01-.27 1.11l-2.2 2.2z"
                      />
                    </svg>
                  </div>
                  <div class="xs:-mt-1 lg:mx-2">
                    <h4 class="font-bold mx-2 text-cyan-400">Phone</h4>
                    <p class="text-white mx-2">+880 1327 2926 90</p>
                  </div>
                </div>

                <div class="flex items-start lg:mx-6 xs:-mx-4">
                  <div class="p-3 lg:rounded-sm xs:rounded-xl text-white lg:-mt-2 xs:-mt-1.5">
                    <svg
                      class="lg:w-10 lg:h-10 md:w-10 md:h-10 xs:w-8 xs:h-8"
                      fill="currentColor"
                      viewBox="0 0 24 24"
                    >
                      <path
                        d="M12 2a7 7 0 00-7 7c0 5.25 7 13 7 13s7-7.75 7-13a7 7 0 00-7-7zm0 9.5a2.5 2.5 0 112.5-2.5 2.5 2.5 0 01-2.5 2.5z"
                      />
                    </svg>
                  </div>
                  <div class="xs:-mt-1 lg:mx-2">
                    <h4 class="font-bold mx-2 text-cyan-400">Location</h4>
                    <p class="text-white mx-2">Sector-6, Uttara, Dhaka-1230, Bangladesh</p>
                  </div>
                </div>
              </div>
            </div>

            <div class="flex space-x-6 xs:mt-10 lg:mt-19 xs:mx-3 lg:mx-12 md:mt-6">
              <a
                href="https://github.com/iamsohan100
"
                target="_blank"
                class="text-cyan-400 border-cyan-400 hover:shadow-cyan-400 hover:text-cyan-400 border duration-500 hover:-translate-y-1.5 p-1.5 rounded-xl transition hover:shadow-[0_0_15px_rgba(0,0,0,0.4)]"
              >
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path
                    d="M12 2.04c-5.52 0-10 4.48-10 
                     10 0 4.42 2.87 8.16 6.84 
                     9.5.5.09.66-.22.66-.48 
                     0-.24-.01-.88-.01-1.72
                     -2.78.6-3.37-1.34-3.37-1.34
                     -.45-1.15-1.11-1.46-1.11-1.46
                     -.9-.61.07-.6.07-.6 
                     1 .07 1.52 1.04 1.52 1.04
                     .89 1.52 2.34 1.08 2.91.83
                     .09-.65.35-1.08.63-1.33
                     -2.22-.26-4.56-1.1-4.56-4.91
                     0-1.08.39-1.96 1.03-2.65
                     -.1-.26-.45-1.31.1-2.74 
                     0 0 .84-.27 2.75 1.03a9.5 
                     9.5 0 015 0c1.91-1.3 
                     2.75-1.03 2.75-1.03.55 
                     1.43.2 2.48.1 2.74.64.69 
                     1.03 1.57 1.03 2.65 0 
                     3.82-2.34 4.65-4.57 
                     4.9.36.31.68.93.68 
                     1.88 0 1.36-.01 2.46-.01 
                     2.79 0 .27.17.58.68.48A10 
                     10 0 0022 12.04c0-5.52-4.48-10-10-10z"
                  />
                </svg>
              </a>

              <!-- Linkedn in -->

              <a
                href="https://www.linkedin.com/in/iamsohan100/"
                target="_blank"
                class="text-cyan-400 border-cyan-400 hover:shadow-cyan-400 hover:text-cyan-400 border duration-500 hover:-translate-y-1.5 p-2 rounded-xl transition hover:shadow-[0_0_15px_rgba(0,0,0,0.4)]"
              >
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                  <path
                    d="M22.23 0H1.77C.79 0 0 .77 0 1.72v20.56C0 23.23.79 24 1.77 24H22.2c.98 0 1.8-.77 1.8-1.72V1.72C24 .77 23.2 0 22.23 0zM7.1 20.44H3.56V9H7.1v11.44zM5.34 7.52c-1.14 0-2.06-.91-2.06-2.03s.92-2.03 2.06-2.03 2.06.91 2.06 2.03-.92 2.03-2.06 2.03zM20.45 20.44h-3.53v-5.65c0-1.35-.03-3.08-1.88-3.08-1.89 0-2.18 1.47-2.18 2.99v5.74H9.33V9h3.39v1.56h.05c.47-.9 1.61-1.86 3.32-1.86 3.56 0 4.22 2.34 4.22 5.37v6.37z"
                  />
                </svg>
              </a>
            </div>
          </div>

          <!-- submit form -->

          <div class="">
            <form
              @submit.prevent="submitForm"
              class="bg-gray-800 rounded-lg xs:-mx-7 shadow-md xs:p-7 lg:p-6 lg:space-y-6 xs:space-y-5 md:space-y-4 xs:mt-5"
            >
              <section class="xs:-mx-4 lg:mx-0">
                <div class="flex items-center justify-center">
                  <h1 class="lg:text-4xl xs:text-2xl font-bold md:-mt-2 lg:mt-3">
                    <span class="text-cyan-500">Contact Me!</span>
                  </h1>
                </div>
                <label for="Name" class="block text-sm font-medium text-white mt-6 mb-1"
                  >Name</label
                >
                <input
                  type="text"
                  id="name"
                  placeholder="Your ame"
                  v-model="name"
                  required
                  class="mt- bg-[#1f242d] text-white block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:ring-white focus:border-blue-500 dark:border-gray-600"
                />
              </section>

              <section class="xs:-mx-4 lg:mx-0">
                <label for="Email" class="block text-sm font-mediu text-white mb-1">Email</label>
                <input
                  type="text"
                  id="email"
                  placeholder="Your Email"
                  v-model="email"
                  required
                  class="mt- bg-[#1f242d] text-white block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:ring-white focus:border-blue-500 dark:border-gray-600"
                />
              </section>
              <!-- <section class="xs:-mx-4 lg:mx-0">
              <label for="Email" class="block text-sm font-mediu text-white mb-1"
                >Phone</label
              >
              <input
                type="text"
                id="phone"
                placeholder="Your Phone"
                v-model="phone"
                required
                class="mt- dark:bg-[#1f242d] block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:ring-white focus:border-blue-500 bg-gray-200 dark:border-gray-600 dark:text-white"
              />
            </section> -->
              <section class="xs:-mx-4 lg:mx-0">
                <label for="Message" class="block text-sm font-medium text-white mb-1"
                  >Message</label
                >
                <textarea
                  id="message"
                  v-model="message"
                  placeholder="Your Message"
                  required
                  class="block bg-[#1f242d] text-white w-full px-3 py-2 border-2 border-gray-300 rounded-md shadow-sm focus:ring-white focus:border-blue-500 dark:border-gray-600"
                  rows="4"
                >
              <!-- dark:bg-[#1f242d] -->
              </textarea
                >
              </section>

              <div class="flex items-center justify-center">
                <button
                  type="submit"
                  class="xs:flex xs:items-center xs:justify-center lg:items-start lg:justify-start lg:block xs:w-40 lg:w-60 md:px-4 shadow-white lg:px-8 xs:py-2 md:py-2.5 text-black bg-[#00f0ff] hover:shadow-[0_0_15px_rgba(0,0,0,0.4)] rounded-full font-medium transition duration-500 hover:shadow-cyan-400 dark:hover:shadow-cyan-400 xs:text-sm lg:text-lg"
                >
                  Send Message
                </button>
              </div>
            </form>
          </div>
        </div>
      </section>
    </section>
  </section>
</template>
