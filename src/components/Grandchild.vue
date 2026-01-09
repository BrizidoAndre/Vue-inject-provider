<script setup>

import {inject} from "vue";
import {commonCount} from "@/utils.js";

const {count} = inject('counter-key');
const {names} = inject('names-key');

function removeLast() {
  names.value.splice(names.value.length - 1, 1);
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
        <h3>Names</h3>
        <button @click="removeLast">Remove last name</button>
        <ul>
          <li v-for="name in names">{{ name }}</li>
        </ul>
      </li>
    </ul>
  </div>
</template>