<script setup lang="ts">
import MainPage from "@/components/MainPage.vue"
import MainLayout from "@/layouts/MainLayout.vue"
import { TooltipProvider } from "#/tooltip"
</script>

<template>
   <TooltipProvider :delayDuration="300">
      <MainLayout>
         <MainPage />
      </MainLayout>
   </TooltipProvider>
</template>
