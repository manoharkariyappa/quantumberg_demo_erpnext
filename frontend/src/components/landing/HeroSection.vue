<script setup>
import DashboardPreview from '@/components/landing/DashboardPreview.vue'
import { useLoginUrl } from '@/composables/useLoginUrl'

const { loginUrl } = useLoginUrl()

const indicators = [
  'Manufacturing, projects & accounting',
  'Live demo environment',
  'Cloud-ready deployment',
]
</script>

<template>
  <section id="home" class="relative overflow-hidden bg-white pb-8 pt-20 sm:pb-10 sm:pt-24 lg:pb-12 lg:pt-24">
    <div
      class="pointer-events-none absolute -right-32 -top-32 h-[420px] w-[420px] rounded-full bg-brand-gradient-soft blur-3xl"
      aria-hidden="true" />
    <div class="pointer-events-none absolute -left-40 top-40 h-[320px] w-[320px] rounded-full bg-edu-purple/5 blur-3xl"
      aria-hidden="true" />

    <div
      class="relative mx-auto grid max-w-7xl items-center gap-8 px-4 sm:px-6 lg:grid-cols-[1fr_1.25fr] lg:gap-12 lg:px-8">
      <div>
        <p
          class="inline-flex items-center gap-2 rounded-full border border-edu-border bg-white px-4 py-1.5 text-body-sm font-semibold text-edu-purple shadow-sm">
          <span class="h-2 w-2 rounded-full bg-brand-gradient" aria-hidden="true" />
          Manufacturing &middot; Projects &middot; Accounting
        </p>

        <h1 class="mt-6 text-display-md font-extrabold text-edu-deep sm:text-display-lg xl:text-display-xl">
          Transform the Way You Manage
          <span class="bg-brand-gradient bg-clip-text text-transparent">Manufacturing, Projects &amp; Accounting</span>
        </h1>

        <p class="mt-5 max-w-2xl text-body-lg text-edu-muted">
          One connected ERPNext workspace for production, project delivery,
          inventory and finance &mdash; so every team works from the same live
          data and every transaction flows straight to the books.
        </p>

        <div class="mt-7 flex flex-col gap-3 sm:flex-row sm:items-center">
          <a :href="loginUrl"
            class="inline-flex items-center justify-center gap-2 rounded-xl bg-brand-gradient px-7 py-3.5 text-body-lg font-semibold text-white shadow-cta transition-transform duration-200 hover:-translate-y-0.5 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-edu-purple focus-visible:ring-offset-2">
            Open Demo App
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"
              stroke-linejoin="round" class="h-4 w-4" aria-hidden="true">
              <path d="M5 12h14M13 6l6 6-6 6" />
            </svg>
          </a>
          <a href="https://www.quantumberg.com/Contact"
            class="inline-flex items-center justify-center gap-2 rounded-xl border-2 border-edu-border bg-white px-7 py-3.5 text-body-lg font-semibold text-edu-ink transition-colors duration-200 hover:border-edu-purple hover:text-edu-purple focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-edu-pink focus-visible:ring-offset-2">
            Schedule Demo
          </a>
        </div>

        <ul class="mt-7 flex flex-wrap items-center gap-x-5 gap-y-2">
          <li v-for="indicator in indicators" :key="indicator"
            class="inline-flex items-center gap-1.5 text-body-sm font-medium text-edu-muted">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"
              stroke-linejoin="round" class="h-3.5 w-3.5 text-edu-pink" aria-hidden="true">
              <path d="M20 6 9 17l-5-5" />
            </svg>
            {{ indicator }}
          </li>
        </ul>
      </div>

      <div class="relative">
        <div class="mx-auto w-[90%] rounded-[26px] bg-brand-gradient p-1.5 shadow-panel" aria-hidden="false">
          <DashboardPreview />
        </div>
      </div>
    </div>
  </section>
</template>
