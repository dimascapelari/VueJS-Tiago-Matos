<template>
  <div :class="baseClass">
    Exemplo 3: Seu formulário foi enviado com sucesso!

    <button @click="onClick()">X</button>
  </div>
</template>

<script>
export default {
  name: "AulaDezesseiEmit",

  props: ["variant", "variant2", "variant3", "text"],

  computed: {
    baseClass() {
      return ["alert", this.variant3 ? `alert-${this.variant3}` : ""];
    },
  },

  methods: {
    onClick() {
      this.$emit("close");
      console.log("clicou");
    },
  },
};
</script>

<style scoped>
.alert {
  display: flex;
  justify-content: space-between;
  padding: 5px;
  border-radius: 6px;
  color: gray;
  background-color: #ddd;
}

.alert-success {
  background-color: #42b983;
  color: #fff;
}

.alert-danger {
  background-color: red;
  color: #fff;
}
</style>
