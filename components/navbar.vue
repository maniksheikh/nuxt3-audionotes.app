<template>
  <nav class="navbar w-full">
    <div class="container mx-auto px-6 py-6">
      <div class="flex justify-between items-center w-[1100px] m-auto">
        <div class="nav-logo">
          <a href="/" class="logo-link">
            <img
              src="https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png"
              srcset="
                https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png?scale-down-to=512   512w,
                https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png?scale-down-to=1024 1024w,
                https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png                    1122w
              "
              sizes="149px"
              alt="Logo"
              style="border-radius: inherit; object-fit: contain"
            />
          </a>
        </div>
        <div class="lg:hidden">
          <button
            @click="toggleMenu"
            class="text-gray-500 focus:outline-none focus:text-gray-700"
          >
            <svg viewBox="0 0 20 20" fill="currentColor" class="menu w-6 h-6">
              <path
                fill-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 100 2h12a1 1 0 100-2H3zm1 5a1 1 0 110-2h12a1 1 0 110 2H4z"
                clip-rule="evenodd"
              ></path>
            </svg>
          </button>
        </div>
        <ul class="lg:flex space-x-5 text-[15px] font-[500]">
          <li
            class="border border-transparent hover:border-[#D9D2C5] hover:bg-[#F5F1EB] px-2 py-2 rounded-md"
          >
            <a href="#">Use Cases</a>
          </li>
          <li
            class="border border-transparent hover:border-[#D9D2C5] hover:bg-[#F5F1EB] px-2 py-2 rounded-md"
          >
            <a href="#">Features</a>
          </li>
          <li
            class="border border-transparent hover:border-[#D9D2C5] hover:bg-[#F5F1EB] px-2 py-2 rounded-md"
          >
            <a href="/pricing">Pricing</a>
          </li>
          <li
            class="border border-transparent hover:border-[#D9D2C5] hover:bg-[#F5F1EB] px-2 py-2 rounded-md"
          >
            <a href="#">Affiliates</a>
          </li>
          <li
            class="border border-transparent hover:border-[#D9D2C5] hover:bg-[#F5F1EB] px-2 py-2 rounded-md"
          >
            <a href="#">Blog</a>
          </li>
        </ul>
        <div
          class="flex items-center justify-center bg-[#ff4f00] text-white font-[600] rounded-full hover:bg-[#ff5100d7] px-2 py-2"
        >
          <a
            href="/"
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
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      showMenu: false,
    };
  },
  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu;
    },
  },
};
</script>

<style scoped>
/* Add your scoped styles here */
</style>
