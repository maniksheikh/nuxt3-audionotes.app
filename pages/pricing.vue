 <template>
  <div class="bg-white py-24">
    <div class="max-w-[1100px] flex mx-auto">
      <div class="w-[600px] m-auto">
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
    </div>
    <div>
      <div class="mt-12">
        <pricing :plans="plansData" />
      </div>
    </div>
  </div>
</template>
  
  <script setup>
</script>
  