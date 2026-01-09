<script setup>
import {ref} from "vue";

const message = ref('');
</script>

<template>
  <p>You're in second place</p>
  <label for="message">State your message</label>
  <input type="text" id="message" v-model="message">
</template>