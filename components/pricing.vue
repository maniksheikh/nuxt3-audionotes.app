<template>
  <div class="grid bg-white grid-cols-1 sm:grid-cols-3 gap-3 px-5 py-5 mt-14">
    <div
      v-for="plan in plans"
      :key="plan.id"
      :class="plan.class"
      :style="plan.css"
      class="bg-[#FFFFFF] border border-gray-200 w-[340px] h-[479px] px-4 py-4 rounded-4xl shadow-md overflow-hidden"
    >
      <div class="p-4">
        <h2 :class="plan.titleCss">{{ plan.name }}</h2>

        <div class="flex items-center">
          <p class="text-[#48404E] font-bold text-[54px]">
            <span>$</span> {{ plan.price }}
          </p>
        </div>

        <div class="mt-4">
          <div>
            <div
              v-for="(feature, index) in plan.features"
              :key="index"
              class="flex gap-2 items-center text-[#666666] mb-2 text-[16px] font-[500]"
            >
              <span>
                <svg
                  class="bg-black rounded-full mr-1"
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
              <span class="opacity-90">{{ feature }}</span>
            </div>
          </div>
        </div>
        <button
          :style="plan.buttonCss"
          class="inline-block mt-6 rounded-3xl px-6 py-2 text-white text-base font-medium text-center bg-blue-500 hover:bg-blue-600"
          @click="startPurchase(plan)"
          :aria-label="plan.buttonText"
          :title="plan.buttonText"
        >
          {{ plan.buttonText }}
        </button>
      </div>
    </div>
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
  