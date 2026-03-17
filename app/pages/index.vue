<script setup lang="ts">
const count = ref(0)

function increment() {
  count.value++
}

function decrement() {
  count.value--
}

function reset() {
  count.value = 0
}
</script>

<template>
  <div class="flex flex-col items-center justify-center min-h-[60vh] gap-12 px-4">
    <div class="flex flex-col items-center gap-2 text-center">
      <h1 class="text-4xl font-bold tracking-tight text-highlighted sm:text-5xl">
        Simple Counter
      </h1>
      <p class="text-lg text-muted max-w-md">
        A minimal counter to get you started. Click the buttons below to change the value.
      </p>
    </div>

    <div class="flex flex-col items-center gap-8">
      <div
        class="text-8xl font-bold tabular-nums text-highlighted transition-all duration-150 select-none sm:text-9xl"
      >
        {{ count }}
      </div>

      <div class="flex items-center gap-3">
        <UButton
          icon="i-lucide-minus"
          size="xl"
          color="neutral"
          variant="outline"
          aria-label="Decrement"
          @click="decrement"
        />
        <UButton
          label="Reset"
          size="xl"
          color="neutral"
          variant="soft"
          @click="reset"
        />
        <UButton
          icon="i-lucide-plus"
          size="xl"
          color="primary"
          aria-label="Increment"
          @click="increment"
        />
      </div>
    </div>

    <UPageCTA
      title="Ready to build something real?"
      description="This starter template comes with Nuxt UI, TypeScript, and everything you need to ship fast."
      variant="subtle"
      :links="[{
        label: 'Get started with Nuxt UI',
        to: 'https://ui.nuxt.com/docs/getting-started/installation/nuxt',
        target: '_blank',
        trailingIcon: 'i-lucide-arrow-right',
        color: 'primary',
        size: 'xl'
      }, {
        label: 'View on GitHub',
        to: 'https://github.com/nuxt-ui-templates/starter',
        target: '_blank',
        icon: 'i-simple-icons-github',
        color: 'neutral',
        variant: 'outline',
        size: 'xl'
      }]"
    />
  </div>
</template>
