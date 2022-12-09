<template>
  <div>
    <TheHeader v-if="showHeader" />
    <h2>Hello Word</h2>
    {{ name }}
    <button @click="showHeader = !showHeader">Ativa e desativa Header</button>
  </div>
</template>

<script>
// import { onBeforeMount, onBeforeUnmount, onUnmounted } from "@vue/runtime-core";
import TheHeader from "./TheHeader.vue";
export default {
  components: { TheHeader },
  name: "AulaDozeCicloDeVidaFileCycle",
  data() {
    return {
      name: "Dimas Capelari",
      showHeader: true,
    };
  },

  // Criação
  // -> Preparar o componente
  // -> Ajax, inicializar algumas variáveis
  // -> Não tem acesso ao template (DOM)

  // Montagem
  // -> Inicializar uma lib externa
  // -> Precisa de acesso ao template (DOM)
  // -> Tem acesso ao template (DOM)

  // Atualização
  // -> Debug
  // -> Update

  // Desmontagem
  // -> Remover tudo que necessário para liberar memória

  // HOOKS

  beforeUpdate() {
    console.log("beforeUpdate");
  },

  updated() {
    console.log("updated");
  },

  //   beforeCreated() {
  //     console.log("beforeCreated");
  //     console.log("Estado:", this.name);
  //     console.log("DOM", this.$el);
  //   },
  //   created() {
  //     console.log("created");
  //     console.log("Estado:", this.name);
  //     console.log("DOM", this.$el);
  //   },
  //   beforeMount() {
  //     console.log("beforeMount");
  //     console.log("Estado:", this.name);
  //     console.log("DOM", this.$el);
  //   },
  //   mounted() {
  //     console.log("mounted");
  //     console.log("Estado:", this.name);
  //     console.log("DOM", this.$el);
  //   },
  //   beforeUnmount() {
  //     console.log("beforeUnmount");
  //   },
  //   unmounted() {
  //     console.log("unmounted");
  //   },
};
</script>

<style></style>
