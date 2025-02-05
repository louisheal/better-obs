<script setup lang="ts">
import { Button } from "#/button"
import { Tooltip, TooltipContent, TooltipTrigger } from "#/tooltip"
</script>

<template>
   <div>
      <Tooltip>
         <TooltipTrigger as-child>
            <Button>Hii</Button>
         </TooltipTrigger>
         <TooltipContent>
            <p>Add to library</p>
         </TooltipContent>
      </Tooltip>
   </div>
</template>

<style scoped></style>
