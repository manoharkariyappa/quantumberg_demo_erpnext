<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  bullets: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <article
    class="flex h-full flex-col rounded-2xl border border-edu-border bg-white p-5 shadow-card transition-all duration-300 hover:-translate-y-1 hover:shadow-card-hover"
  >
    <span class="inline-flex h-10 w-10 items-center justify-center rounded-lg bg-brand-gradient text-white shadow-cta">
      <slot name="icon">
        <svg
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="h-5 w-5"
          aria-hidden="true"
        >
          <circle cx="12" cy="8" r="4" />
          <path d="M4 21v-1a6 6 0 0 1 6-6h4a6 6 0 0 1 6 6v1" />
        </svg>
      </slot>
    </span>

    <h3 class="mt-3 text-[16px] font-bold text-edu-deep">
      {{ title }}
    </h3>
    <p class="mt-1 text-body-sm text-edu-muted">
      {{ description }}
    </p>

    <ul class="mt-4 space-y-1.5">
      <li
        v-for="bullet in bullets"
        :key="bullet"
        class="flex items-start gap-2 text-body-sm text-edu-ink"
      >
        <svg
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2.5"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="mt-1 h-3.5 w-3.5 shrink-0 text-edu-pink"
          aria-hidden="true"
        >
          <path d="M20 6 9 17l-5-5" />
        </svg>
        {{ bullet }}
      </li>
    </ul>
  </article>
</template>
