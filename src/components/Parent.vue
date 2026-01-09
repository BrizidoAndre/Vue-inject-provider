<script setup>
import Child from "@/components/Child.vue"
import {provide, ref} from "vue";

const count = ref(0);

const names = ref(["André", 'Matheus', 'Lucas', 'João', 'Eduardo', 'Enzo', 'Luan', 'Arthur'])


provide('counter-key', {
  count
})
provide('names-key', {
  names
})
</script>

<template>
  <div class="box">
    <h1>Parent component</h1>
    <p>Current count: {{ count }}</p>
    <Child/>
  </div>
</template>