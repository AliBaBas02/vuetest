<script setup>

import Test2 from "./components/test2.vue";
import Test from "./components/test.vue";
import {onMounted, ref} from "vue";

let num2 = ref("styl")
let num = ref(1)
let str = ref([
  {name:"styl", id: 1},
  {name:"kostas", id: 2}
])
let change = ref(null);


</script>

<template>
  <p ref="change">Troll Mode {{num2}}</p>
  <div :style="{fontSize: num + 'px'}">
  <Test2
  v-for="x in str"
  :num2="x.name"
  @enlarge-text="num += 1"
  />
  </div>
  <Test/>
  <Test>Troll</Test>

</template>

<style scoped>
.highlighted{
  background: yellow;
}
</style>
