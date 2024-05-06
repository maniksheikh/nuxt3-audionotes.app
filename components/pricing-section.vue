<template>
  <div class="rounded-xl m-auto">
    <div class="flex items-center justify-center m-auto">
      <div class="flex items-center gap-2 bg-[#F0F0F0] rounded-[50px] p-[5px]">
        <button
          @click="viewMonthlyPayment"
          class="text-base py-2 px-5 text-[#464343] opacity-80 rounded-[50px] font-bold"
          :class="{
            'bg-gradient-to-br to-[white] from-[white] text-black':
              planType === 'monthly',
          }"
          aria-label="Monthly"
          title="Monthly"
        >
          Monthly
        </button>
        <button
          @click="viewAnnualPayment"
          class="text-base py-2 px-5 text-[#464343] opacity-80 rounded-[50px] font-bold"
          :class="{
            'bg-gradient-to-br to-[white] from-[white] text-black':
              planType === 'annual',
          }"
          aria-label="Annual"
          title="Annual"
        >
          Annual
        </button>
        <button
          @click="viewLifetimePayment"
          class="text-base py-2 px-5 text-[#464343] opacity-80 rounded-[50px] font-bold"
          :class="{
            'bg-gradient-to-br to-[white] from-[white] text-black':
              planType === 'lifetime',
          }"
          aria-label="Lifetime"
          title="Lifetime"
        >
          Lifetime
        </button>
      </div>
    </div>

    <div class="mt-12 w-[1100px] m-auto">
      <pricing :plans="plansData" />
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";
import plans from "~/static/plans.json";

const planType = ref("monthly");

const viewMonthlyPayment = () => {
  planType.value = "monthly";
};
const viewAnnualPayment = () => {
  planType.value = "annual";
};
const viewLifetimePayment = () => {
  planType.value = "lifetime";
};
const plansData = computed(() => {
  const selectedPlan = plans[planType.value];

  if (planType.value === "lifetime" && !selectedPlan) {
    return {
      name: "lifetime",
      price: "Your lifetime price",
      features: ["Feature 1", "Feature 2", "Feature 3"],
    };
  }
  return selectedPlan;
});
</script>

<style lang="scss" scoped></style>
