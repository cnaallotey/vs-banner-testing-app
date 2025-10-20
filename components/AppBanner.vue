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
      src: `http://localhost:3000/js?affiliate=${props.affiliate}&type=top&closeable=true`,
    },
  ],
})
</script>

<template>
    <div>
        
    </div>
</template>