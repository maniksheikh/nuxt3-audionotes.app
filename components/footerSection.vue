<template>
  <div class="mt-20 pb-32 sm:pb-0 sm:px-2">
    <div class="max-w-[1100px] bg-[black] rounded-3xl sm:rounded-none m-auto">
      <div
        class="bg-[black] p-14 sm:p-5 sm:mt-10 text-center rounded-3xl m-auto"
      >
        <h1 class="text-[50px] sm:text-[36px] font-[600] text-white">
          Unleash the power of Voice notes with AI
        </h1>
        <button
          class="flex max-w-[215px] justify-center items-center m-auto mt-10 bg-[#ff4f00] text-white rounded-full hover:bg-red-400 px-3 py-3"
        >
          <span
            class="text-center text-[18px] sm:text-[16px] font-[500] sm:font-[400] items-center"
            >Get Started Now</span
          >
          <img
            src="https://framerusercontent.com/images/QDgxMHJz2vKvFSMvhZpA6xplIBM.svg"
            alt=""
            class="ml-1 w-4 h-4"
            style="object-fit: cover; border-radius: inherit"
          />
        </button>
      </div>
      <div
        class="flex sm:block px-10 items-center justify-between p-10 gap-10 text-white"
      >
        <div>
          <p class="text-[15px] leading-7 opacity-70">
            Audionotes(www.audionotes.app) <br />
            <span
              >AudioNotes is an AI-First Note Taking App <br />
              that summarizes your voice and text notes, <br />
              helps you generate content.
            </span>
          </p>
          <p class="mt-5 sm:mt-5 opacity-80 text-[18px]">a1811 Labs product</p>
          <br />
        </div>
        <div class="text-left">
          <div
            class="flex justify-center text-[16.5px] sm:text-[15px] sm:justify-between"
          >
            <div class="flex sm:block justify-between">
              <div class="px-7 sm:px-0 opacity-75">
                <ul>
                  <li
                    class="transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="/" class="nuxt-link"> Home </NuxtLink>
                  </li>
                  <li
                    class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="#" class="nuxt-link"> Blog </NuxtLink>
                  </li>
                  <li
                    class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="/pricing" class="nuxt-link">
                      Pricing
                    </NuxtLink>
                  </li>
                  <li
                    class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="#" class="nuxt-link"> Mobile App </NuxtLink>
                  </li>
                </ul>
              </div>
              <div class="sm:mt-5 px-7 sm:px-0 opacity-75">
                <ul>
                  <li
                    class="transition-all font-semibold duration-300 ease-in-outhover:text-gray-300"
                  >
                    <NuxtLink to="#" class="nuxt-link"> Features </NuxtLink>
                  </li>
                  <li
                    class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="/faqs" class="nuxt-link"> FAQS </NuxtLink>
                  </li>
                  <li
                    class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="/pricing" class="nuxt-link">
                      Web App
                    </NuxtLink>
                  </li>
                </ul>
              </div>
            </div>
            <div class="flex sm:block sm:pl-0 justify-between">
              <div class="px-7 sm:px-0 opacity-75">
                <ul>
                  <li
                    class="transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="#" class="nuxt-link">
                      Terms of service
                    </NuxtLink>
                  </li>
                  <li
                    class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="/faqs" class="nuxt-link">
                      Privacy policy
                    </NuxtLink>
                  </li>
                  <li
                    class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="/pricing" class="nuxt-link">
                      Support
                    </NuxtLink>
                  </li>
                </ul>
              </div>
              <div class="px-7 sm:px-0 sm:mt-10 opacity-75">
                <ul>
                  <li
                    class="transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="#" class="nuxt-link">Podonotes </NuxtLink>
                  </li>
                  <li
                    class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="/faqs" class="nuxt-link">
                      Avatarize
                    </NuxtLink>
                  </li>
                  <li
                    class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-gray-300"
                  >
                    <NuxtLink to="/pricing" class="nuxt-link">
                      HeadlinesAI
                    </NuxtLink>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="sm:p-5 py-5 copy-right-content">
        <p class="text-white text-center opacity-90 justify-center pb-3">
          © Copyright {{ new Date().getFullYear() }} -
          <span class="name">AudioNotes.app</span>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style>
</style>