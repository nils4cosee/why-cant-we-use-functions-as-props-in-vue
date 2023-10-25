<script setup lang="ts">
import {ref} from "vue";
import {Button} from "./Button.ts";

const clicks = ref<string[]>([])

const buttons: Button[] = [
  {
    label: "A",
    onClick: () => {
      clicks.value.push("A")
    }
  },
  {
    label: "B",
    onClick: () => {
      clicks.value.push("B")
    }
  }
]

</script>

<template>
  <h1>Why can't we use functions as props?</h1>
  <Buttons :buttons="buttons"/>
  <div>
    &nbsp; <span v-for="click in clicks">{{click}} </span>
  </div>
</template>
