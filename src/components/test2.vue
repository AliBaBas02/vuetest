<script setup>
import { ref} from "vue";

const styl = defineProps({
  num2: String,
})
defineEmits(['enlarge-text'])

</script>

<template>
<ul>
  <li>{{num2}}</li>
</ul>
  <button @click="$emit('enlarge-text',)">Enlarge text</button>
</template>

<style scoped>

</style>