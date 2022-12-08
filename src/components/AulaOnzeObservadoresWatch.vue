<template>
  <div>
    <input v-model="name" type="text" />
    <br />
    {{ name }}

    <br />
    <br />

    <select v-model="pageCount">
      <option value="5">5</option>
      <option value="10">10</option>
      <option value="15">15</option>
    </select>
    <br />
    {{ pageCount }}
    <br />
    <br />

    <input type="text" v-model="user.first_name" />
    <br />
    <input type="text" v-model="user.last_name" />
    <br />
    {{ user.first_name }} {{ user.last_name }}
    <br />
    <br />
  </div>
</template>

<script>
export default {
  name: "AulaOnzeObservadoresWatch",
  data() {
    return {
      name: "",
      pageCount: 5,
      user: {
        first_name: "",
        last_name: "",
      },
    };
  },
  watch: {
    name(valor) {
      if (valor.length >= 3) {
        this.saveUserName();
      }
    },
    pageCount() {
      this.changePage();
    },
    user: {
      handler() {
        console.log("User alterado");
      },
      deep: true,
    },
  },
  methods: {
    saveUserName() {
      console.log(this.name);
    },
    changePage() {
      console.log("Ajax changePage");
    },
  },
};
</script>

<style></style>
