<script setup lang="ts">
import { Button } from "#/button"
import { TextTooltip } from "#/text-tooltip"
</script>

<template>
   <div>
      <TextTooltip text="Your tooltip text">
         <Button>Hover me</Button>
      </TextTooltip>
   </div>
</template>

<style scoped></style>
