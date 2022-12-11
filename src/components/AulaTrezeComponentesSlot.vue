<template>
  <div>
    <slot />
    <slot name="description" />
    <slot name="teste" v-if="$slots.teste" />
  </div>
</template>

<script>
export default {
  name: "AulaTrezeComponentesSlot",

  mounted() {
    // consigo acessar todos elementos do componente
    console.log(this.$el);

    // consigo acessar todos os slots do componente
    console.log(this.$slots);
  },
};
</script>

<style></style>
