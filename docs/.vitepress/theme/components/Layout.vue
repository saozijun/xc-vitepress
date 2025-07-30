<script setup>
import DefaultTheme from "vitepress/theme";
import { toggleDark } from "../utils/Dark";
import SplashCursor from "./SplashCursor.vue";
import Progress from "./Progress.vue";
import Music from "./Music.vue";
import Lt from "./Lt.vue";
import NavTitle from "./NavTitle.vue";
import { onMounted, onUnmounted } from "vue";

toggleDark();
const { Layout } = DefaultTheme;
</script>

<template>
  <Progress />
  <Layout>
    <template #nav-bar-title-after>
      <ClientOnly>
        <NavTitle />
      </ClientOnly>
    </template>
    <template #layout-bottom>
      <Music />
      <SplashCursor />
    </template>
    <template #aside-outline-before>
      <Lt />
    </template>
  </Layout>
</template>

<style scoped>
:deep(.VPNav) {
  transform: translateY(0);
  transition: transform 0.3s ease-in-out;
}
:deep(.VPNav.nav-hidden) {
  transform: translateY(-100%);
}

:deep(.VPNavScreen) {
  height: 100vh;
}
:deep(.VPLocalNav) {
  display: none;
}
</style>
