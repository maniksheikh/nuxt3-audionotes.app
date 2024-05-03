<template>
  <div class="grid grid-cols-4 sm:grid-cols-1 two-column-grid gap-4 mt-8">
    <div
      v-for="plan in plans"
      :key="plan.id"
      :class="plan.class"
      :style="plan.css"
    >
      <div>
        <h2 :class="plan.titleCss">{{ plan.name }}</h2>
        <h2 class="text-base mb-5 text-[#343434] leading-8">
          {{ plan.description }}
        </h2>
        <div class="flex">
          <p class="text-[#48404E] font-extrabold text-5xl sm:text-4xl mb-3">
            <span>$</span>{{ plan.price }}
          </p>
          <p class="text-base text-[#48404E] font-medium mt-6 sm:mt-4">
            {{ plan.billingCycle }}
          </p>
        </div>
        <small class="text-[#7D6E7D]">{{ plan.billingType }}</small>
        <div>
          <p class="text-[#48404E] font-semibold text-lg py-4">
            Package Includes:
          </p>
          <div>
            <div
              v-for="(feature, index) in plan.features"
              :key="index"
              class="flex gap-2 items-center text-[#666666] mb-2 text-sm"
            >
              <span>
                <svg
                  width="18"
                  height="18"
                  viewBox="0 0 18 18"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M7.1627 13.5002L2.8877 9.22519L3.95645 8.15645L7.1627 11.3627L14.0439 4.48145L15.1127 5.5502L7.1627 13.5002Z"
                    fill="#34A853"
                  />
                </svg>
              </span>
              {{ feature }}
            </div>
          </div>
        </div>
        <button
          :style="plan.buttonCss"
          class="inline-block w-full mt-6 rounded-lg px-6 py-2 text-white text-base font-medium text-center"
          @click="startPurchase(plan)"
          :aria-label="plan.buttonText"
          :title="plan.buttonText"
        >
          {{ plan.buttonText }}
        </button>
      </div>
    </div>
    <div></div>
  </div>
</template>
  
  <script setup>
const props = defineProps({
  plans: {
    type: Array,
    required: true,
  },
});

function startPurchase(plan) {
  if (!store.user) {
    signInWithGoogle();
    return;
  }
  if (plan.id === "free") {
    navigateTo("/app");
    return;
  }

  eventLog("begin_checkout", {
    tier: plan.name,
    uid: store.user.uid,
    price: plan.price,
  });

  try {
    const paymentUrl = `${plan.link}?prefilled_email=${encodeURIComponent(
      store.userDetails.email
    )}`;
    window.location.href = paymentUrl;

    eventLog("checkout_progress", {
      tier: plan.name,
      uid: store.user.uid,
      price: plan.price,
    });
  } catch (error) {
    console.error("Error during payment redirection:", error);
  }
}
</script>
  <style scoped>
@media screen and (min-width: 700px) and (max-width: 1024px) {
  .two-column-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}
</style>
  