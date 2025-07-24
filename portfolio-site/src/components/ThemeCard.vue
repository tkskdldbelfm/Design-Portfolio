<!-- @format -->

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ThemedCard",
});
</script>

<template>
  <div class="rounded-xl border bg-background text-foreground shadow-md p-6 transition-colors">
    <h2 class="text-xl font-bold">테마 카드</h2>
    <p class="text-sm mt-2"> 현재 테마에 따라 배경과 텍스트 색상이 바뀝니다. </p>
  </div>
</template>
