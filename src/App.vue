<template>
  <Home nombre="Jesner" apellido="Ramirez" />
  <!-- <div>{{ text }}</div> -->
  <!-- <div id="aqui"></div>
  <h1>Opacity CSS VueJs</h1>
  <button @click="show = !show">Menu</button>
  <transition name="fade">
    <Menu v-show="show" />
  </transition>
  <h1>Modal</h1>
  <div>
    <Modal />
  </div> -->
  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  <!-- <component
    :is="componente"
    v-bind="{ msg: 'Welcome to Your Vue.js App' }"
  ></component> -->
</template>

<script>
import Home from "./components/Home.vue";
import { provide } from "vue";
// import Menu from "./components/Menu.vue";
// import Modal from "./components/Modal.vue";
// import { defineAsyncComponent } from "vue";
// import HelloWorld from "./components/HFelloWorld.vue";
// el defineAsyncComponent hace que cargue el componente cuando recien se va a utilizar, asi optimizamos los componentes para que cargue solamente cuando sea necesario y asi hacer que las paginas no demoren en cargar.

// const HelloWorld = defineAsyncComponent(() =>
//   import("./components/HelloWorld.vFue")
// );

export default {
  name: "App",
  components: {
    // // HelloWorld,
    // Menu,
    // Modal,
    Home,
  },
  setup() {
    provide("username", "JesnerRa");
    provide("a", "aaa");
  },
  data() {
    return {
      // componente: "HelloWorld",
      // show: false,
      // text: "Hola vue",
    };
  },
  beforeCreate() {},
  created() {},
  mounted() {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
.fade-leave-active,
.fade-enter-active {
  transition: opacity 0.5s ease;
}
</style>
