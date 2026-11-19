<script setup>
import RoleCard from '@/components/landing/RoleCard.vue'

const roles = [
  {
    key: 'production',
    title: 'Production Teams',
    description:
      'A focused workspace for the people running the shop floor.',
    bullets: [
      'Plan and track work orders from release to completion',
      'Work with bills of materials, routings and production schedules',
      'Record quality checks and material consumption',
    ],
    icon: 'production',
  },
  {
    key: 'projects',
    title: 'Project Teams',
    description:
      'Tools that keep projects, tasks and delivery on track.',
    bullets: [
      'Plan projects, milestones and task dependencies',
      'Assign resources and monitor progress in real time',
      'Track timesheets and project costs',
    ],
    icon: 'projects',
  },
  {
    key: 'finance',
    title: 'Finance & Operations',
    description:
      'A connected financial view across the whole business.',
    bullets: [
      'Manage ledgers, receivables, payables and cash flow',
      'Track production, inventory and project costs',
      'Monitor margins and performance from live dashboards',
    ],
    icon: 'finance',
  },
]
</script>

<template>
  <section id="roles" class="scroll-mt-24 bg-white py-6 lg:py-8">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="mx-auto max-w-3xl text-center">
        <p class="text-body-sm font-bold uppercase tracking-[0.18em] text-edu-purple">
          Built for every role
        </p>
        <h2 class="mt-2 text-display-sm font-extrabold text-edu-deep sm:text-display-md">
          One platform, every team
        </h2>
        <p class="mt-3 text-body-lg text-edu-muted">
          Production, project and finance teams each get a workspace shaped
          around their work &mdash; while the underlying records stay connected.
        </p>
      </div>

      <div class="mt-5 grid gap-4 md:grid-cols-3">
        <RoleCard
          v-for="role in roles"
          :key="role.key"
          :title="role.title"
          :description="role.description"
          :bullets="role.bullets"
        >
          <template #icon>
            <svg
              v-if="role.icon === 'production'"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="h-5 w-5"
              aria-hidden="true"
            >
              <path d="M3 21V9l6 4V9l6 4V5l6 4v12H3z" />
              <path d="M7 17h2" />
              <path d="M13 17h2" />
            </svg>
            <svg
              v-else-if="role.icon === 'projects'"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="h-5 w-5"
              aria-hidden="true"
            >
              <rect x="3" y="3" width="18" height="18" rx="2" />
              <path d="M9 3v18" />
              <path d="M3 9h18" />
            </svg>
            <svg
              v-else-if="role.icon === 'finance'"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="h-5 w-5"
              aria-hidden="true"
            >
              <path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20" />
              <path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z" />
              <path d="M9 7h6" />
              <path d="M9 11h4" />
            </svg>
            <svg
              v-else
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="h-5 w-5"
              aria-hidden="true"
            >
              <rect x="3" y="3" width="7" height="9" rx="1.5" />
              <rect x="14" y="3" width="7" height="5" rx="1.5" />
              <rect x="14" y="12" width="7" height="9" rx="1.5" />
              <rect x="3" y="16" width="7" height="5" rx="1.5" />
            </svg>
          </template>
        </RoleCard>
      </div>
    </div>
  </section>
</template>
