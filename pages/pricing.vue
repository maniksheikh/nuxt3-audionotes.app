 <template>
  <div class="bg-white py-24 xl:px-6 sm:py-12">
    <div class="max-w-[1100px] flex mx-auto">
      <div class="max-w-[600px] mx-auto">
        <h2 class="text-[#343434] text-[46px] font-bold leading-relaxed">
          Plans & Pricing
        </h2>
        <p class="text-[#9e9898] text-[18px] font-medium leading-6 mt-3">
          Save Upto 50% with our Annual Plans:
        </p>
      </div>
      <div class="w-[100%]">
        <pricing-section></pricing-section>
      </div>

      <div
        v-if="isBangladeshi"
        class="w-[100%] px-[4rem] sm:px-[0rem] xl:px-[0rem] mt-10"
      >
        <bkash :pricing="pricingData"></bkash>
      </div>
    </div>
  </div>
</template>
  
  <script setup>
import pricingData from "~/static/pricing.json";
const isBangladeshi = ref(false);
</script>
  