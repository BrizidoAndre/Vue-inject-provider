<script setup>
import {ref} from "vue";

const count = ref(0)
</script>

<template>
  <p>You're in first place</p>
  <p>State your count {{ count }}</p>
  <button @click="count++">+</button>
</template>
