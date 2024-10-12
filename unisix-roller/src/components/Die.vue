<script setup lang="js">
import { ref } from "vue";

const { maxValue, currentValue } = defineProps({
  maxValue: String,
  currentValue: Number,
});
let _maxValue = Number(maxValue);

function getRandomInt(min, max) {
  min = Math.ceil(min);
  max = Math.floor(max);
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
</script>
<template>
  <div class="die">
    <button type="button" @click="">
      value is {{ getRandomInt(1, _maxValue) }} /
      {{ maxValue }}
    </button>
  </div>
</template>

<style scoped>
.die {
  display: inline-block;
  float: left;
  width: 100px;
  height: 50px;
}
</style>
