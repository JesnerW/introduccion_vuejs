<template>
  <!-- <div>{{ firstName }} {{ lastName }}</div>
  <div>{{ fullName }}</div> -->
  <div>Props: {{ fullName2 }}</div>
  <div>Provide:Inject : {{ username }} {{ a }}</div>
  <button ref="btn">Click!</button>
  <!-- <div>{{ text }}</div> -->
  <!-- <div>{{ counter }}</div> -->
  <!-- <div>{{ obj }}</div> -->
</template>

<script setup>
// import { onMounted } from "vue";
import {
  defineProps,
  defineExpose,
  ref,
  toRefs,
  watch,
  computed,
  inject,
} from "vue"; // toRefs sirve para la reatividad de
// import { ref, computed } from "vue";
// import { reactive, watch } from "vue"; // solo recomendado para Objetos
const props = defineProps({
  nombre: String,
  apellido: String,
});

const { nombre, apellido } = toRefs(props);

const fullName2 = computed(() => {
  return `${nombre.value} ${apellido.value}`;
});

const username = inject("username");
const a = inject("a");

const btn = ref(null);

watch(btn, (value) => {
  console.log(value);
});

defineExpose({
  fullName2,
});

// const firstName = ref("Jesner");
// const lastName = ref("Ramirez");
// const text = ref("Hola Vue");

// const counter = ref(0);
// setInterval(() => counter.value++, 500);

// const obj = reactive({ counter: 0 });
// setInterval(() => obj.counter++, 500);

// watch(
//   () => obj.counter,
//   (valor, anterior) => {
//     console.log(valor, anterior);
//   }
// );
// const fullName = computed(() => {
//   return `${firstName.value} ${lastName.value}`;
// });
</script>
