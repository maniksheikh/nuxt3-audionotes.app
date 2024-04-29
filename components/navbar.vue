<template>
  <nav class="navbar w-[100%]">
  <div class="container mx-auto px-4 py-4">
    <div class="flex justify-between items-center w-[1100px] m-auto">
      <div class="nav-logo">
        <nuxt-link to="/" class="logo-link">
          <img
            src="https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png"
            srcset="
              https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png?scale-down-to=512   512w,
              https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png?scale-down-to=1024 1024w,
              https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png                    1122w
            "
            sizes="149px"
            alt="Logo"
            style="border-radius: inherit; object-fit: contain;"
          />
        </nuxt-link>
      </div>

      <ul class="flex space-x-6 text-gray-800 text-md font-semibold">
        <li class="hover:bg-zinc-200 px-2 py-2 rounded-md"><nuxt-link to="#">Use Cases</nuxt-link></li>
        <li class="hover:bg-zinc-200 px-2 py-2 rounded-md"><nuxt-link to="#">Features</nuxt-link></li>
        <li class="hover:bg-zinc-200 px-2 py-2 rounded-md"><nuxt-link to="#">Pricing</nuxt-link></li>
        <li class="hover:bg-zinc-200 px-2 py-2 rounded-md"><nuxt-link to="#">Affiliates</nuxt-link></li>
        <li class="hover:bg-zinc-200 px-2 py-2 rounded-md"><nuxt-link to="#">Blog</nuxt-link></li>
      </ul>

      <div class="flex items-center bg-[#ff4f00] text-white rounded-full hover:bg-[#ff5100d7] px-4 py-2">
        <nuxt-link to="/" aria-label="Try For Free" title="Try For Free" class="flex items-center">
          <span>Try For Free</span>
          <img
            src="https://framerusercontent.com/images/QDgxMHJz2vKvFSMvhZpA6xplIBM.svg"
            alt=""
            class="ml-1 w-4 h-4"
            style="object-fit: cover; border-radius: inherit;"
          />
        </nuxt-link>
      </div>
    </div>
  </div>
</nav>

</template>