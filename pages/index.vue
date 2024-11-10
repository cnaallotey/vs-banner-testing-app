<script setup>
const { query } = useRoute()
const affiliate = ref('')

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
  "vuejsforege",
  "nuxtnation",
  "angulartraining",
  "vuejs"
]

const showBanner = ref(true)

function openURL () {
  window.location.href = `/?affiliate=${affiliate.value}`
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
      <USelectMenu v-model="affiliate" @change="openURL()" :options="affiliates" />
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