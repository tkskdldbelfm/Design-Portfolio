<!-- @format -->

<script setup lang="ts">
import { defineComponent, ref, onMounted } from "vue";

const theme = ref<"light" | "dark">("light");

onMounted(() => {
  const saved = localStorage.getItem("theme");
  if (saved === "dark") {
    document.documentElement.classList.add("dark");
    theme.value = "dark";
  }
});

function toggleTheme() {
  const isDark = document.documentElement.classList.contains("dark");
  if (isDark) {
    document.documentElement.classList.remove("dark");
    localStorage.setItem("theme", "light");
    theme.value = "light";
  } else {
    document.documentElement.classList.add("dark");
    localStorage.setItem("theme", "dark");
    theme.value = "dark";
  }
}
</script>

<template>
  <button class="rounded-full p-2 border bg-background text-foreground shadow transition" @click="toggleTheme">
    {{ theme === "dark" ? "🌙 다크" : "☀️ 라이트" }}
  </button>
</template>
