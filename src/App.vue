<script setup>
import Parent from "@/components/Parent.vue";
import Inside from "@/components/Inside.vue";
import {ref} from "vue";
import FirstPlace from "@/components/FirstPlace.vue";
import SecondPlace from "@/components/SecondPlace.vue";

const name = ref();
const currentPlace = ref(0);
const places = [
  FirstPlace,
  SecondPlace
]
</script>

<template>
  <Parent/>
  <Inside>
    <template #header>
      <h2>
        Custom Header
      </h2>
    </template>
    <h1>Custom Main</h1>
    <template #footer>
      <p>
        <strong>
          Custom footer
        </strong>
      </p>
    </template>
  </Inside>
  <label for="first">First</label>
  <input type="radio" name="places" id="first" value="0" v-model="currentPlace">
  <label for="second">Second</label>
  <input type="radio" name="places" id="second" value="1" v-model="currentPlace">
  <div>
    <keep-alive>
      <component :is="places[currentPlace]"></component>
    </keep-alive>
  </div>
</template>

