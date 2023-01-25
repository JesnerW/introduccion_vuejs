<template>
  <div>
    <button @click="toggle">Modal</button>
    <teleport to="#aqui">
      <div v-show="show" class="modal">
        <h1>Titulo</h1>
        <p>Lorem ipsum dolor sit amet.</p>
        <button @click="toggle">Cerrar</button>
      </div>
    </teleport>
    <!-- el teleport funciona cuando el destino esta declarado antes del componente
    
    App.vue Line 2
    Teleport declarado Line 4 AQUI
  --></div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
    };
  },
  methods: {
    toggle() {
      this.show = !this.show;
    },
  },
};
</script>
