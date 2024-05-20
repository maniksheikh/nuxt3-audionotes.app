<template>
  <div>
    <div class="flex w-[100%] mx-auto p-4 py-5">
      <div class="flex justify-between items-center w-[1070px] m-auto">
        <div class="nav-logo">
          <nuxt-link to="/" class="logo-link">
            <img
              decoding="async"
              sizes="149px"
              srcset="
                https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png?scale-down-to=512   512w,
                https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png?scale-down-to=1024 1024w,
                https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png                    1122w
              "
              src="https://framerusercontent.com/images/xBz63gfbPpHJjmQFD32STgtCgfE.png"
              alt=""
              style="
                display: block;
                width: 100%;
                height: 100%;
                border-radius: inherit;
                object-position: center;
                object-fit: contain;
                image-rendering: auto;
              "
            />
          </nuxt-link>
        </div>

        <div class="hidden sm:block">
          <ul class="flex space-x-3 text-[#535251] text-[15px] font-[500]">
            <li
              class="border border-transparent hover:bg-[#F5F1EB] hover:border-[#D9D2C5] p-2 py-1 hover:rounded-md font-semibold"
            >
              <nuxt-link to="#">Use Cases</nuxt-link>
            </li>
            <li
              class="border border-transparent hover:bg-[#F5F1EB] hover:border-[#D9D2C5] p-2 py-1 hover:rounded-md font-semibold"
            >
              <nuxt-link to="#">Features</nuxt-link>
            </li>
            <li
              class="border border-transparent hover:bg-[#F5F1EB] hover:border-[#D9D2C5] p-2 py-1 hover:rounded-md font-semibold"
            >
              <nuxt-link to="/pricing">Pricing</nuxt-link>
            </li>
            <li
              class="border border-transparent hover:bg-[#F5F1EB] hover:border-[#D9D2C5] p-2 py-1 hover:rounded-md font-semibold"
            >
              <nuxt-link to="#">Affiliates</nuxt-link>
            </li>
            <li
              class="border border-transparent hover:bg-[#F5F1EB] hover:border-[#D9D2C5] p-2 py-1 hover:rounded-md font-semibold"
            >
              <nuxt-link to="#">Blog</nuxt-link>
            </li>
          </ul>
        </div>

        <div class="cursor-pointer sm:hidden">
          <img
            @click="isShowMobileNav = !isShowMobileNav"
            decoding="async"
            src="https://framerusercontent.com/images/dG1Azogn9b3q4VAzzfU8jvuvqo.svg"
            alt=""
            style="
              display: block;
              width: 100%;
              height: 100%;
              border-radius: inherit;
              object-position: center center;
              object-fit: cover;
              image-rendering: auto;
            "
          />
        </div>

        <div
          class="items-center bg-[#ff4f00] text-white rounded-full px-3 py-2 sm:block hidden"
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
        </div>
      </div>
    </div>
    <mobile-nav v-show="isShowMobileNav"></mobile-nav>
  </div>
</template>

<script setup>
const isShowMobileNav = ref(false);
</script>

<style scoped></style>