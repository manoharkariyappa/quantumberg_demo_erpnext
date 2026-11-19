<script setup>
import DashboardPreview from '@/components/landing/DashboardPreview.vue'

const benefits = [
  {
    title: 'One source of operational truth',
    description:
      'BOMs, work orders, projects, stock and ledgers live in one system instead of scattered spreadsheets.',
  },
  {
    title: 'Production and project coordination',
    description:
      'Shop-floor, procurement and delivery teams work from the same schedules, orders and resource information.',
  },
  {
    title: 'Real-time financial visibility',
    description:
      'Sales, purchases, payments and expenses post directly to accounting as work happens.',
  },
  {
    title: 'Accurate production and project costing',
    description:
      'Track material, labour and timesheet costs against project budgets and work order estimates.',
  },
  {
    title: 'Faster billing and collections',
    description:
      'Convert approved timesheets and completed work into invoices without re-entering the same details.',
  },
  {
    title: 'Less repetitive administrative work',
    description:
      'Quality checks, stock movements, invoices and payments flow through connected records and approvals.',
  },
]
</script>

<template>
  <section class="scroll-mt-24 bg-edu-bg py-6 lg:py-8">
    <div class="mx-auto grid max-w-7xl items-center gap-6 px-4 sm:px-6 lg:grid-cols-[1.6fr_1fr] lg:gap-8 lg:px-8">
      <div class="relative order-2 lg:order-1">
        <div class="mx-auto w-[90%] rounded-[26px] bg-brand-gradient p-1.5 shadow-panel">
          <DashboardPreview src="proj-admin-dashboard.png" />
        </div>
      </div>

      <div class="order-1 lg:order-2">
        <p class="text-body-sm font-bold uppercase tracking-[0.18em] text-edu-purple">
          Benefits
        </p>
        <h2 id="benefits" class="mt-2 text-display-sm font-extrabold text-edu-deep sm:text-display-md">
          Run production, projects and finance with
          <span class="bg-brand-gradient bg-clip-text text-transparent">
            less friction
          </span>
        </h2>
        <p class="mt-3 text-body-lg text-edu-muted">
          From the shop floor to the project board and the balance sheet, the
          platform keeps operational and financial data connected &mdash; so
          coordination improves and manual admin drops.
        </p>

        <ul class="mt-4 space-y-2.5">
          <li v-for="benefit in benefits" :key="benefit.title" class="flex gap-4">
            <span
              class="mt-0.5 inline-flex h-5 w-5 shrink-0 items-center justify-center rounded-full bg-brand-gradient text-white">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round"
                stroke-linejoin="round" class="h-3.5 w-3.5" aria-hidden="true">
                <path d="M20 6 9 17l-5-5" />
              </svg>
            </span>
            <div>
              <h3 class="text-[15px] font-bold text-edu-deep">
                {{ benefit.title }}
              </h3>
              <p class="mt-0.5 text-body-sm text-edu-muted">
                {{ benefit.description }}
              </p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
