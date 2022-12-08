<template>
  <div>
    <button @click="onClick">Enviar</button>
  </div>
  <br />
  <br />
  <div @mouseover.once="onMouseOver" @mouseout.once="onMouseOut">
    Mouse over
  </div>
  <br />
  <br />

  <div>
    <form action="https://google.com" @submit.prevent="onSubmit">
      <input type="text" @keyup="onKeyUp" />
      <button type="submit">Google</button>
    </form>
  </div>
</template>

<script>
export default {
  methods: {
    onClick($evt) {
      console.log("click", $evt);
    },
    onMouseOver($evt) {
      console.log("mouse over", $evt);
    },
    onMouseOut($evt) {
      console.log("mouse out", $evt);
    },
    onSubmit($evt) {
      console.log("Submit", $evt);
    },
    onKeyUp($evt) {
      console.log("onKeyUp", $evt);
    },
  },
};
</script>

<style></style>
