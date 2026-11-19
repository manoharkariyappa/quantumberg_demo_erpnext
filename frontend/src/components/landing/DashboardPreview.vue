<script setup>
import { computed } from 'vue'

const props = defineProps({
  src: {
    type: String,
    default: 'admin-dashboard.png',
  },
})

const resolvedSrc = computed(
  () => `${import.meta.env.BASE_URL}${props.src.replace(/^\/+/, '')}`,
)
</script>

<template>
  <figure class="relative overflow-hidden rounded-2xl border border-edu-border shadow-panel" role="img"
    aria-label="Preview of the ERPNext dashboard showing production, work orders, projects and accounting">
    <img :src="resolvedSrc" alt="" class="block h-auto max-h-[390px] w-full object-cover object-top">
  </figure>
</template>
