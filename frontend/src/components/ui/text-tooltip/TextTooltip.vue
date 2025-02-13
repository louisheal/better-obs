<script setup lang="ts">
import { Tooltip, TooltipContent, TooltipTrigger } from "#/tooltip"

defineProps<{
   text: string
}>()
</script>

<template>
   <Tooltip>
      <TooltipTrigger>
         <slot />
      </TooltipTrigger>
      <TooltipContent class="tooltip">
         {{ text }}
      </TooltipContent>
   </Tooltip>
</template>

<style>
/**
* Everything below here can be removed when shadcn-vue moves to Tailwind v4
* https://github.dev/unovue/shadcn-vue/blob/5572de2b9e1f9002184a3bf197e71c27187af76b/apps/www/src/lib/registry/default/ui/tooltip/TooltipContent.vue
*/
.tooltip {
   z-index: 50;
   overflow: hidden;
   border-radius: 6px;
   border: 1px solid var(--color-border);
   background-color: var(--color-popover);
   padding: 0.375rem 0.75rem;
   font-size: 0.875rem;
   color: var(--color-popover-foreground);
   box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1);
   animation:
      fadeIn 0.2s ease-out forwards,
      zoomIn 0.2s ease-out forwards;
}

.tooltip[data-state="closed"] {
   animation: fadeOut 0.15s ease-out forwards;
}

.tooltip[data-side="bottom"] {
   animation:
      fadeIn 0.2s ease-out forwards,
      zoomIn 0.2s ease-out forwards,
      slideFromTop 0.2s ease-out forwards;
}

.tooltip[data-side="left"] {
   animation:
      fadeIn 0.2s ease-out forwards,
      zoomIn 0.2s ease-out forwards,
      slideFromRight 0.2s ease-out forwards;
}

.tooltip[data-side="right"] {
   animation:
      fadeIn 0.2s ease-out forwards,
      zoomIn 0.2s ease-out forwards,
      slideFromLeft 0.2s ease-out forwards;
}

.tooltip[data-side="top"] {
   animation:
      fadeIn 0.2s ease-out forwards,
      zoomIn 0.2s ease-out forwards,
      slideFromBottom 0.2s ease-out forwards;
}

@keyframes fadeIn {
   0% {
      opacity: 0;
   }
   100% {
      opacity: 1;
   }
}

@keyframes fadeOut {
   0% {
      opacity: 1;
   }
   100% {
      opacity: 0;
   }
}

@keyframes zoomIn {
   0% {
      transform: scale(0.95);
   }
   100% {
      transform: scale(1);
   }
}

@keyframes slideFromTop {
   0% {
      transform: translateY(-0.5rem);
   }
   100% {
      transform: translateY(0);
   }
}

@keyframes slideFromRight {
   0% {
      transform: translateX(0.5rem);
   }
   100% {
      transform: translateX(0);
   }
}

@keyframes slideFromLeft {
   0% {
      transform: translateX(-0.5rem);
   }
   100% {
      transform: translateX(0);
   }
}

@keyframes slideFromBottom {
   0% {
      transform: translateY(0.5rem);
   }
   100% {
      transform: translateY(0);
   }
}
</style>
