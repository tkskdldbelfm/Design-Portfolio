<!-- @format -->

<script setup lang="ts">
import DarkModeToggle from "./DarkmodeToggle.vue";
import ThemeCard from "./ThemeCard.vue";
defineProps<{ msg: string }>();
</script>

<template>
  <div class="fixed top-4 right-4">
    <DarkModeToggle />
  </div>
  <div>
    <ThemeCard />
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
