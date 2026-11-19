<script setup>
import { useLoginUrl } from '@/composables/useLoginUrl'

const { loginUrl } = useLoginUrl()
</script>

<template>
  <section id="get-started" class="relative overflow-hidden bg-brand-gradient py-7 lg:py-8">
    <div class="pointer-events-none absolute inset-0 opacity-[0.12]" aria-hidden="true" style="
        background-image: radial-gradient(circle at 20% 20%, #fff 1px, transparent 1px);
        background-size: 22px 22px;
      " />

    <div class="relative mx-auto max-w-4xl px-4 text-center sm:px-6 lg:px-8">
      <h2 class="text-display-sm font-extrabold text-white sm:text-display-md">
        Ready to Connect Manufacturing, Projects &amp; Accounting?
      </h2>
      <p class="mx-auto mt-3 max-w-2xl text-body-lg text-white/85">
        Bring production, project delivery, inventory and finance together in
        one connected platform.
      </p>

      <div class="mt-4 flex flex-col items-center justify-center gap-3 sm:flex-row">
        <a :href="loginUrl"
          class="inline-flex w-full items-center justify-center gap-2 rounded-xl bg-white px-6 py-3 text-body-lg font-semibold text-edu-purple shadow-panel transition-transform duration-200 hover:-translate-y-0.5 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-offset-2 focus-visible:ring-offset-edu-purple sm:w-auto">
          Open Demo App
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"
            stroke-linejoin="round" class="h-4 w-4" aria-hidden="true">
            <path d="M5 12h14M13 6l6 6-6 6" />
          </svg>
        </a>

        <a href="https://www.quantumberg.com/Contact"
          class="inline-flex w-full items-center justify-center rounded-xl border-2 border-white/70 px-6 py-3 text-body-lg font-semibold text-white transition-colors duration-200 hover:bg-white/10 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-offset-2 focus-visible:ring-offset-edu-purple sm:w-auto">
          Schedule Demo
        </a>
      </div>
    </div>
  </section>
</template>
