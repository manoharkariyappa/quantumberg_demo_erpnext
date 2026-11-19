<script setup>
import FeatureCard from '@/components/landing/FeatureCard.vue'

const features = [
  {
    title: 'Production Planning',
    description:
      'Plan capacity, schedules and material requirements across every production line.',
    icon: 'production',
    accent: 'purple',
  },
  {
    title: 'Bill of Materials',
    description:
      'Maintain multi-level BOMs, routings and costs for accurate production planning.',
    icon: 'bom',
    accent: 'emerald',
  },
  {
    title: 'Work Orders',
    description:
      'Release, track and complete work orders with real-time shop-floor visibility.',
    icon: 'workorder',
    accent: 'pink',
  },
  {
    title: 'Quality Management',
    description:
      'Capture inspections, quality checks and non-conformances at every stage.',
    icon: 'quality',
    accent: 'blue',
  },
  {
    title: 'Inventory & Stock',
    description:
      'Track raw materials, work in progress and finished goods across warehouses.',
    icon: 'inventory',
    accent: 'amber',
  },
  {
    title: 'Project Management',
    description:
      'Plan projects, milestones and dependencies with clear ownership and timelines.',
    icon: 'project',
    accent: 'cyan',
  },
  {
    title: 'Task & Resource Tracking',
    description:
      'Assign tasks, monitor progress and balance workloads across teams.',
    icon: 'tasks',
    accent: 'orange',
  },
  {
    title: 'Timesheets & Billing',
    description:
      'Record billable time and turn approved work into accurate project invoices.',
    icon: 'timesheet',
    accent: 'rose',
  },
  {
    title: 'Financial Accounting',
    description:
      'Keep ledgers, journals and trial balances accurate and always up to date.',
    icon: 'accounting',
    accent: 'indigo',
  },
  {
    title: 'Invoicing & Payments',
    description:
      'Manage sales invoices, purchase bills, receipts and payment follow-ups.',
    icon: 'invoicing',
    accent: 'emerald',
  },
  {
    title: 'Cost Centers & Budgeting',
    description:
      'Track production and project costs against budgets with clear cost centers.',
    icon: 'budgeting',
    accent: 'blue',
  },
  {
    title: 'Analytics & Reports',
    description:
      'Get live dashboards for production, projects, cash flow and profitability.',
    icon: 'analytics',
    accent: 'purple',
  },
]
</script>

<template>
  <section class="scroll-mt-24 bg-white py-6 lg:py-8">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="mx-auto max-w-3xl text-center">
        <p class="text-body-sm font-bold uppercase tracking-[0.18em] text-edu-purple">
          Features
        </p>
        <h2 id="features" class="mt-2 text-display-sm font-extrabold text-edu-deep sm:text-display-md">
          Everything you need to run
          <span class="bg-brand-gradient bg-clip-text text-transparent">
            manufacturing, projects and accounting
          </span>
        </h2>
        <p class="mt-3 text-body-lg text-edu-muted">
          Connected capabilities for the shop floor, project delivery and
          finance &mdash; from the bill of materials to the project board and
          the general ledger.
        </p>
      </div>

      <div class="mt-5 grid gap-3 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 lg:gap-4">
        <FeatureCard
          v-for="(feature, index) in features"
          :key="feature.title"
          :title="feature.title"
          :description="feature.description"
          :accent="feature.accent"
          :index="index"
        >
          <template #icon>
            <svg v-if="feature.icon === 'production'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <path d="M3 21V9l6 4V9l6 4V5l6 4v12H3z" />
              <path d="M7 17h2" />
              <path d="M13 17h2" />
            </svg>
            <svg v-else-if="feature.icon === 'bom'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <path d="m12 2 9 5-9 5-9-5 9-5z" />
              <path d="m3 12 9 5 9-5" />
              <path d="m3 17 9 5 9-5" />
            </svg>
            <svg v-else-if="feature.icon === 'workorder'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <rect x="8" y="2" width="8" height="4" rx="1" />
              <path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2" />
              <path d="M9 12h6" />
              <path d="M9 16h6" />
            </svg>
            <svg v-else-if="feature.icon === 'quality'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z" />
              <path d="m9 12 2 2 4-4" />
            </svg>
            <svg v-else-if="feature.icon === 'inventory'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <path d="M21 8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z" />
              <path d="m3.3 7 8.7 5 8.7-5" />
              <path d="M12 22V12" />
            </svg>
            <svg v-else-if="feature.icon === 'project'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <rect x="3" y="3" width="18" height="18" rx="2" />
              <path d="M9 3v18" />
              <path d="M3 9h18" />
            </svg>
            <svg v-else-if="feature.icon === 'tasks'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <rect x="3" y="3" width="18" height="18" rx="2" />
              <path d="m9 12 2 2 4-4" />
            </svg>
            <svg v-else-if="feature.icon === 'timesheet'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <circle cx="12" cy="12" r="9" />
              <path d="M12 7v5l3 2" />
            </svg>
            <svg v-else-if="feature.icon === 'accounting'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20" />
              <path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z" />
              <path d="M9 7h6" />
              <path d="M9 11h4" />
            </svg>
            <svg v-else-if="feature.icon === 'invoicing'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <path d="M4 2v20l2-1 2 1 2-1 2 1 2-1 2 1 2-1V2l-2 1-2-1-2 1-2-1-2 1-2-1z" />
              <path d="M8 7h8" />
              <path d="M8 11h8" />
              <path d="M8 15h5" />
            </svg>
            <svg v-else-if="feature.icon === 'budgeting'" viewBox="0 0 24 24" fill="none" stroke="currentColor"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <path d="M21.21 15.89A10 10 0 1 1 8 2.83" />
              <path d="M22 12A10 10 0 0 0 12 2v10z" />
            </svg>
            <svg v-else viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"
              stroke-linejoin="round" class="h-5 w-5" aria-hidden="true">
              <line x1="18" y1="20" x2="18" y2="10" />
              <line x1="12" y1="20" x2="12" y2="4" />
              <line x1="6" y1="20" x2="6" y2="14" />
            </svg>
          </template>
        </FeatureCard>
      </div>
    </div>
  </section>
</template>
