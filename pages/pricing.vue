<template>
  <div class="bg-white py-24 xl:px-6 sm:py-12">
    <div class="max-w-[1300px] mx-auto">
      <div class="max-w-[600px] mx-auto text-center mb-20">
        <h2
          class="text-[#343434] text-5xl sm:text-[28px] font-bold leading-relaxed"
        >
          Simple <span class="boujee-text">Pricing.</span>
        </h2>
        <p class="text-[#666666] text-lg font-medium leading-8 mt-4">
          Choose the plan that fits your budget & learning style, with clear
          benefits and no surprises.
        </p>
      </div>
      <pricing-section></pricing-section>
      <div
        v-if="isBangladeshi"
        class="max-w-[100%] px-[4rem] sm:px-[0rem] xl:px-[0rem] mt-10"
      >
        <bkash :pricing="pricingData"></bkash>
      </div>
    </div>
  </div>
</template>
  
  <script setup>
import pricingData from "~/static/pricing.json";
const isBangladeshi = ref(false);

const fetchData = async () => {
  try {
    const { data } = await $axios.get("https://api.country.is");
    isBangladeshi.value = data.country === "BD";
  } catch (error) {
    console.error("Error fetching country data:", error);
  }
};

onMounted(fetchData);
</script>
  