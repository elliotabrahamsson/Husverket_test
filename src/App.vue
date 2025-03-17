<script setup>
import MainContent from "./components/MainContent.vue";
import Sidebar from "./components/Sidebar.vue";
import Header from "./components/Header.vue";
</script>

<template>
  <div class="flex h-screen">
    <Sidebar />
    <div class="flex flex-col flex-1">
      <Header class="ml-4 space-x-3" />
      <MainContent class="flex-1" />
    </div>
  </div>
</template>
