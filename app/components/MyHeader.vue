<script setup lang="ts">
const { items } = mainNav()
</script>

<template>
  <UHeader>
    <template #title>
     <img
         src="/favicon.svg"
         alt="logo"
         class="h-8 w-8"
     />
      R. Gibson
    </template>

    <UNavigationMenu :items="items" class="hidden lg:flex" />

    <template #right>
      <div class="hidden lg:flex items-center gap-1.5">
        <UColorModeButton />

        <UTooltip text="Open on GitHub" :kbds="['meta', 'G']">
          <UButton
              color="neutral"
              variant="ghost"
              to="https://github.com/legendairy75"
              target="_blank"
              icon="i-simple-icons-github"
              aria-label="GitHub"
          />
        </UTooltip>
        <UTooltip text="Open on Linkedin" :kbds="['meta', 'G']">
          <UButton
              color="neutral"
              variant="ghost"
              to="https://www.linkedin.com/in/cameron-gibson-ab10461a8"
              target="_blank"
              icon="i-simple-icons-linkedin"
              aria-label="LinkedIn"
          />
        </UTooltip>
      </div>
    </template>

    <template #body>
      <div class="flex flex-col gap-6">
        <UNavigationMenu :items="items" orientation="vertical" class="-mx-2.5" />

        <div class="flex flex-col gap-2">
          <UColorModeButton class="w-full justify-center" />

          <UButton
              color="neutral"
              variant="outline"
              to="https://github.com/legendairy75"
              target="_blank"
              icon="i-simple-icons-github"
              label="GitHub"
              block
          />

          <UButton
              color="neutral"
              variant="outline"
              to="https://www.linkedin.com/in/cameron-gibson-ab10461a8"
              target="_blank"
              icon="i-simple-icons-linkedin"
              label="LinkedIn"
              block
          />
        </div>
      </div>
    </template>
  </UHeader>
</template>
