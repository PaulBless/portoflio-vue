<template>
  <nav
    class="p-3 border-gray-200 rounded bg-green-100 dark:bg-gray-800 dark:border-gray-700">
    <div class="container flex flex-wrap items-center justify-between mx-auto">
      <p class="flex items-center hover:underline">
        <img src="../assets/img/iampaul-logo.png" class="h-6 mr-5 sm:h-10 invisible" />
        <span
          class="self-center hover:text-green-700 text-xl font-semibold whitespace-nowrap dark:text-white">
          <a href="/" class="">Paul Eshun</a>
        </span>
      </p>

      <div class="hidden w-full md:block md:w-auto">
        <ul
          class="flex flex-col mt-4 rounded-lg text-lg bg-gray-50 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium md:border-0 md:bg-transparent dark:bg-gray-800 md:dark:bg-transparent dark:border-gray-700">
          <li>
            <router-link
              to="/"
              class="flex items-center hover:text-green-700 hover:underline bg-green-50 p-2 ml-2 text-gray-900 rounded-lg dark:text-white hover:bg-green-100 dark:hover:bg-gray-700"
              aria-current="page">
              <svg
                aria-hidden="true"
                class="flex-shrink-0 w-6 h-6 text-green-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg">
                <path
                  clip-rule="evenodd"
                  fill-rule="evenodd"
                  d="M9.293 2.293a1 1 0 011.414 0l7 7A1 1 0 0117 11h-1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-3a1 1 0 00-1-1H9a1 1 0 00-1 1v3a1 1 0 01-1 1H5a1 1 0 01-1-1v-6H3a1 1 0 01-.707-1.707l7-7z"></path>
              </svg>
              <span class="flex-1 ml-2 whitespace-nowrap">Home</span>
            </router-link>
          </li>
          <li>
            <router-link
              to="/projects"
              class="flex items-center hover:text-green-700 hover:underline p-2 ml-2 text-gray-900 rounded-lg dark:text-white hover:bg-green-100 dark:hover:bg-gray-700"
              aria-current="page">
              <svg
                aria-hidden="true"
                class="flex-shrink-0 w-6 h-6 text-green-500 transition duration-75 dark:text-gray-400 dark:group-hover:text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg">
                <path
                  d="M2 4.25A2.25 2.25 0 014.25 2h2.5A2.25 2.25 0 019 4.25v2.5A2.25 2.25 0 016.75 9h-2.5A2.25 2.25 0 012 6.75v-2.5zM2 13.25A2.25 2.25 0 014.25 11h2.5A2.25 2.25 0 019 13.25v2.5A2.25 2.25 0 016.75 18h-2.5A2.25 2.25 0 012 15.75v-2.5zM11 4.25A2.25 2.25 0 0113.25 2h2.5A2.25 2.25 0 0118 4.25v2.5A2.25 2.25 0 0115.75 9h-2.5A2.25 2.25 0 0111 6.75v-2.5zM15.25 11.75a.75.75 0 00-1.5 0v2h-2a.75.75 0 000 1.5h2v2a.75.75 0 001.5 0v-2h2a.75.75 0 000-1.5h-2v-2z"></path>
              </svg>
              <span class="flex-1 ml-2 whitespace-nowrap">Projects</span>
            </router-link>
          </li>
          
          <li>
            <router-link
              to="/about"
              class="flex items-center p-2 ml-2 hover:text-green-700 hover:underline text-gray-900 rounded-lg dark:text-white hover:bg-green-100 dark:hover:bg-gray-700"
              aria-current="page">
              <svg
                aria-hidden="true"
                class="flex-shrink-0 w-6 h-6 text-green-500 hover:text-green-700 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg">
                <path
                  clip-rule="evenodd"
                  fill-rule="evenodd"
                  d="M10.868 2.884c-.321-.772-1.415-.772-1.736 0l-1.83 4.401-4.753.381c-.833.067-1.171 1.107-.536 1.651l3.62 3.102-1.106 4.637c-.194.813.691 1.456 1.405 1.02L10 15.591l4.069 2.485c.713.436 1.598-.207 1.404-1.02l-1.106-4.637 3.62-3.102c.635-.544.297-1.584-.536-1.65l-4.752-.382-1.831-4.401z"></path>
              </svg>
              <span class="flex-1 ml-2 whitespace-nowrap">About</span>
            </router-link>
          </li>
          
          <li>
            <router-link
              to="/contact"
              class="flex items-center p-2 ml-2 hover:text-green-700 hover:underline text-gray-900 rounded-lg dark:text-white hover:bg-green-100 dark:hover:bg-gray-700"
              aria-current="page">

              <svg width="20px" height="20px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" stroke="#198754">
                <g id="SVGRepo_bgCarrier" stroke-width="0"/>
                <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"/>
                <g id="SVGRepo_iconCarrier"> 
                <path d="M3.51089 2L7.15002 2.13169C7.91653 2.15942 8.59676 2.64346 8.89053 3.3702L9.96656 6.03213C10.217 6.65159 10.1496 7.35837 9.78693 7.91634L8.40831 10.0375C9.22454 11.2096 11.4447 13.9558 13.7955 15.5633L15.5484 14.4845C15.9939 14.2103 16.5273 14.1289 17.0314 14.2581L20.5161 15.1517C21.4429 15.3894 22.0674 16.2782 21.9942 17.2552L21.7705 20.2385C21.6919 21.2854 20.8351 22.1069 19.818 21.9887C6.39245 20.4276 -1.48056 1.99997 3.51089 2Z" stroke="" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/> </g>

              </svg>
              <span class="flex-1 ml-2 whitespace-nowrap">Contact</span>
            </router-link>
          </li>
          <li>
            <router-link
              to="/blog"
              class="flex hidden items-center p-2 ml-2 hover:text-green-700 hover:underline text-gray-900 rounded-lg dark:text-white hover:bg-green-100 dark:hover:bg-gray-700"
              aria-current="page">
              <svg
                aria-hidden="true"
                class="flex-shrink-0 w-6 h-6 text-green-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg">
                <path
                  clip-rule="evenodd"
                  fill-rule="evenodd"
                  d="M1 5.25A2.25 2.25 0 013.25 3h13.5A2.25 2.25 0 0119 5.25v9.5A2.25 2.25 0 0116.75 17H3.25A2.25 2.25 0 011 14.75v-9.5zm1.5 5.81v3.69c0 .414.336.75.75.75h13.5a.75.75 0 00.75-.75v-2.69l-2.22-2.219a.75.75 0 00-1.06 0l-1.91 1.909.47.47a.75.75 0 11-1.06 1.06L6.53 8.091a.75.75 0 00-1.06 0l-2.97 2.97zM12 7a1 1 0 11-2 0 1 1 0 012 0z"></path>
              </svg>
              <span class="flex-1 ml-2 whitespace-nowrap">Blogs</span>
            </router-link>
          </li>

          <!-- language link item -->
          <li
            class="hidden lg:flex items-center border border-gray-500 hover:bg-green-100 rounded-lg px-4 py-1 md:order-2">
            
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      active: 0,
      logo: '../assets/dev.png',
    };
  },
  methods: {
    inActive() {
      this.active += 1;
    },
  },
};
</script>

<style>
.tester-color{
  color: #123456;
}
.fade-nav-enter-active,
.fade-nav-leave-active {
  transition: opacity 0.5s ease;
}

.fade-nav-enter-from,
.fade-nav-leave-to {
  opacity: 0;
}

.vue-school-active-link {
  background-color: rgb(225, 255, 228);
  padding: 5px 12px;
  border-radius: 10px;
  text-decoration: none;
}
</style>
