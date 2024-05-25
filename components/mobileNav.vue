<template>
  <div class="pb-5 hidden sm:block">
    <ul
      class="block text-[#535251] text-[18px] px-3 p-3 text-center font-[600]"
    >
      <li class="p-2 py-1 hover:rounded-md font-semibold">
        <nuxt-link to="#">Use Cases</nuxt-link>
      </li>
      <li class="p-2 py-1 hover:rounded-md font-semibold">
        <nuxt-link to="#">Features</nuxt-link>
      </li>
      <li class="p-2 py-1 hover:rounded-md font-semibold">
        <nuxt-link to="/pricing">Pricing</nuxt-link>
      </li>
      <li class="p-2 py-1 hover:rounded-md font-semibold">
        <nuxt-link to="#">Affiliates</nuxt-link>
      </li>
      <li class="p-2 py-1 hover:rounded-md font-semibold">
        <nuxt-link to="#">Blog</nuxt-link>
      </li>
    </ul>

    <button
      class="flex justify-center text-center bg-[#ff4f00] m-auto text-white text-[15px] rounded-full px-3.5 py-2.5"
    >
      <nuxt-link
        to="/"
        aria-label="Try For Free"
        title="Try For Free"
        class="flex items-center"
      >
        <span>Try For Free</span>
        <img
          src="https://framerusercontent.com/images/QDgxMHJz2vKvFSMvhZpA6xplIBM.svg"
          alt=""
          class="ml-1 w-4 h-4"
          style="object-fit: cover; border-radius: inherit"
        />
      </nuxt-link>
    </button>
  </div>
</template>
  
  <script setup>
const isShowMobileNav = ref(false);
</script>
  
  <style lang="scss" scoped></style>