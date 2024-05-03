<template>
  <div class="rounded-xl mx-auto">
    <div class="flex items-center justify-end">
      <div class="flex items-center gap-2 bg-[#F6EFEF] rounded-[50px] p-[5px]">
        <button
          @click="viewMonthlyPayment"
          class="text-base py-2.5 px-5 text-[#FF6B00] hover:bg-[#EDB74D] rounded-[50px] font-bold"
          :class="{
            'bg-gradient-to-br to-[#FF6B00] from-[#EDB74D] text-[white]':
              planType === 'monthly',
          }"
          aria-label="Monthly"
          title="Monthly"
        >
          Monthly
        </button>
        <button
          @click="viewAnnualPayemnt"
          class="text-base py-3 px-5 text-[#FF6B00] hover:bg-[#EDB74D] rounded-[50px] font-bold"
          :class="{
            'bg-gradient-to-br to-[#FF6B00] from-[#EDB74D] text-[white]':
              planType === 'annual',
          }"
          aria-label="annual"
          title="Annual"
        >
          Annual
        </button>
        <button
          @click="viewLifetimePayment"
          class="text-base py-3 px-5 text-[#FF6B00] hover:bg-[#EDB74D] rounded-[50px] font-bold"
          :class="{
            'bg-gradient-to-br to-[#FF6B00] from-[#EDB74D] text-[white]':
              planType === 'lifetime',
          }"
          aria-label="lifetime"
          title="lifetime"
        >
          Lifetime
        </button>
      </div>
    </div>
    <div class="text-end pr-2 mt-2">
      <p v-show="planType === 'yearly'" class="text-[#9B9DB6] text-base">
        Save 20% with yearly plan.
      </p>
      <p v-show="planType === 'monthly'" class="text-[#9B9DB6] text-base">
        More expensive but cancel anytime.
      </p>
    </div>
    <div class="mx-auto mt-12">
      <pricing :plans="plansData" />
    </div>
  </div>
</template>

<script setup>
import plans from "~/static/plans.json";

const planType = ref("yearly");

const viewAnnualPayemnt = () => {
  planType.value = "annual";
};
const viewMonthlyPayment = () => {
  planType.value = "monthly";
};
const viewLifetimePayment = () => {
  planType.value = "lifetime";
};
const plansData = computed(() => {
  return plans[planType.value];
});
</script>

<style lang="scss" scoped></style>