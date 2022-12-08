<template>
  <h3>V-show</h3>
  <div v-show="showName">
    Nome: {{ firstName }}<br />
    Sobrenome: {{ lastName }}
  </div>

  <hr />

  <h3>V-if</h3>
  <div v-if="accessLevel === 'admin'">Usuário Admin</div>
  <div v-else-if="accessLevel === 'marketing'">Usuário Marketing</div>
  <div v-else>Usuário Normal</div>

  <hr />
</template>

<script>
export default {
  data() {
    return {
      showName: true,
      firstName: "Dimas",
      lastName: "Capelari",
      accessLevel: "marketing",
    };
  },
};
</script>

<style></style>
