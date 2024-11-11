<script setup>
const { query } = useRoute()
const affiliate = ref('')

const unListedAffiliate = ref('')

const affiliates = [
  "masteringnuxt",
  "vueschool",
  "vueschool_premium",
  "vueschool_free",
  "vs_masteringpinia",
  "vueuse",
  "pinia",
  "vuerouter",
  "NSCRIPT",
  "vuejsnation",
  "vuejsforge",
  "nuxtnation",
  "angulartraining",
  "vuejs",
  "vuejsdevelopers",
  "nuxt"
]

const showBanner = ref(true)

function openURL (id) {
  window.location.href = `/?affiliate=${id}`
}

onMounted(() => {
  if (query.affiliate) {
    affiliate.value = query.affiliate
  }
})
</script>

<template>
    <div class="w-full h-lvh flex justify-center items-center p-4 md:p-10">
    <div class="max-w-md flex flex-col gap-4 w-full">
    <AppBanner :affiliate="affiliate" :key="affiliate" />
    <p class="text-gray-700 font-medium">Select your affiliate</p>
      <USelectMenu v-model="affiliate" @change="openURL(affiliate)" :options="affiliates" />

      <form action="submit" @submit.prevent="openURL(unListedAffiliate)" class="flex flex-col gap-2 mt-6">
        <p class="text-gray-700 font-medium">Enter your affiliate id if not listed</p>
        <UInput v-model="unListedAffiliate" />
        <UButton type="submit" class="w-full inline-flex items-center justify-center text-center">Submit</UButton>
      </form>
    </div>
      
    </div>
</template>

<style>
body, html {
  scroll-behavior: smooth;
  margin: 0;
  padding: 0;
}
#bb-banner-video {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
}
</style>