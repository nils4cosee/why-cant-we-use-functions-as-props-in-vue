<script setup lang="ts">

import type {Button} from "./Button.ts"

const props = defineProps<{
  buttons: Button[]
}>()

</script>
<template>
  <div>
    <button v-for="button in props.buttons" @click="button.onClick">
      {{ button.label }}
    </button>
  </div>
</template>

