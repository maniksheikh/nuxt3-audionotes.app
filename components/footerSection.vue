<template>
  <div class="pb-32">
    <div class="mt-10 w-[1100px] bg-[black] rounded-3xl m-auto">
      <div class="w-[1100px] bg-[black] p-16 text-center rounded-3xl m-auto">
        <h1 class="text-[52px] font-[600] text-white">
          Unleash the power of Voice notes with <br />
          AI
        </h1>
        <div
          class="flex w-[215px] justify-center items-center m-auto mt-10 bg-[#ff4f00] text-white rounded-full hover:bg-red-400 px-4 py-4"
        >
          <a
            href="/"
            aria-label="Try For Free"
            title="Try For Free"
            class="flex items-center"
          >
            <span class="text-center text-[18px] font-[500] items-center"
              >Get Started Now</span
            >
            <img
              src="https://framerusercontent.com/images/QDgxMHJz2vKvFSMvhZpA6xplIBM.svg"
              alt=""
              class="ml-1 w-4 h-4"
              style="object-fit: cover; border-radius: inherit"
            />
          </a>
        </div>
      </div>
      <div class="flex justify-between p-14 gap-10 text-white">
        <div>
          <p class="text-[16px] leading-7 opacity-70">
            Audionotes(www.audionotes.app) <br />
            <span
              >AudioNotes is an AI-First Note Taking App <br />
              that summarizes your voice and text notes, <br />
              helps you generate content.
            </span>
          </p>
          <br />
          <p class="opacity-80 text-[18px]">a1811 Labs product</p>
        </div>
        <div class="flex">
          <div class="px-10 opacity-75">
            <ul>
              <li
                class="transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="#" class="nuxt-link"> Home </NuxtLink>
              </li>
              <li
                class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="#" class="nuxt-link"> Blog </NuxtLink>
              </li>
              <li
                class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="/pricing" class="nuxt-link"> Pricing </NuxtLink>
              </li>
              <li
                class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="#" class="nuxt-link"> Mobile App </NuxtLink>
              </li>
            </ul>
          </div>
          <div class="px-10 opacity-75">
            <ul>
              <li
                class="transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="#" class="nuxt-link"> Features </NuxtLink>
              </li>
              <li
                class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="/faqs" class="nuxt-link"> FAQS </NuxtLink>
              </li>
              <li
                class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="/pricing" class="nuxt-link"> Web App </NuxtLink>
              </li>
            </ul>
          </div>
          <div class="px-10 opacity-75">
            <ul>
              <li
                class="transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="#" class="nuxt-link"> Terms of service </NuxtLink>
              </li>
              <li
                class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="/faqs" class="nuxt-link">
                  Privacy policy
                </NuxtLink>
              </li>
              <li
                class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="/pricing" class="nuxt-link"> Support </NuxtLink>
              </li>
            </ul>
          </div>
          <div class="px-5 opacity-75">
            <ul>
              <li
                class="transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="#" class="nuxt-link">Podonotes </NuxtLink>
              </li>
              <li
                class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="/faqs" class="nuxt-link"> Avatarize </NuxtLink>
              </li>
              <li
                class="pt-2 transition-all font-semibold duration-300 ease-in-out hover:text-yellow-400"
              >
                <NuxtLink to="/pricing" class="nuxt-link">
                  HeadlinesAI
                </NuxtLink>
              </li>
            </ul>
          </div>
        </div>
      </div>

      <div class="copy-right-content">
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