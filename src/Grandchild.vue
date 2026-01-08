<script setup>

import {inject} from "vue";
import {commonCount} from "@/utils.js";

const {count} = inject('counter-key');
const {names} = inject('names-key');

function removeLast() {
  const lastIndex = names.value.length;
  names.value.splice(lastIndex, 1);
}
</script>

<template>
  <div class="box">
    <h3>Grandchild Component</h3>
    <ul>
      <li>
        <p>Count from Parent: <strong>{{ count }}</strong></p>
        <input type="text" v-model="count">
      </li>
      <li>
        <p>Global count from main.js: <strong>{{ commonCount }}</strong></p>
        <input type="text" v-model="commonCount">
      </li>
      <li>
        <h3>Names</h3>
        <ul>
          <li v-for="name in names">{{ name }}</li>
        </ul>
        <button @click="removeLast">Remove last name</button>
      </li>
    </ul>

  </div>
</template>