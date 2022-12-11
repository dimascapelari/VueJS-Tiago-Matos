<template>
  <div
    :class="[
      'alert',
      {
        'alert-success': variant === 'success',
        'alert-danger': variant === 'danger',
      },
    ]"
  >
    Exemplo 1: Seu formulário foi enviado com sucesso!
  </div>

  <br />
  <div
    :class="[
      'alert',
      {
        'alert-success': variant2 === 'success',
        'alert-danger': variant2 === 'danger',
      },
    ]"
  >
    {{ text }}
  </div>
  <br />
  <div :class="baseClass">
    Exemplo 3: Seu formulário foi enviado com sucesso!
  </div>
</template>

<script>
export default {
  name: "AulaQuinzeProps",

  props: ["variant", "variant2", "variant3", "text"],

  computed: {
    baseClass() {
      return ["alert", this.variant3 ? `alert-${this.variant3}` : ""];
    },
  },
};
</script>

<style scoped>
.alert {
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
