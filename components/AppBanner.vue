<script setup>
const props = defineProps({
    affiliate: {
        type: String,
        required: true
    }
})

useHead({
  script: [
    {
      src: `https://staging-banner.bitterbrains.com/js?affiliate=${props.affiliate}&type=top&closeable=true`,
    },
  ],
})
</script>

<template>
    <div>
        
    </div>
</template>