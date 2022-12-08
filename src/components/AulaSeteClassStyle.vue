<template>
  <h1 :class="{ title: true, 'title-home': isHome }">Curso Vue 3</h1>

  <p :class="pClass">
    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Deleniti ratione
    nobis deserunt non odio culpa reprehenderit impedit voluptate iusto dolor
    reiciendis ipsa, facilis eligendi vel ut ea consequuntur hic animi.
  </p>

  <p :style="styleClass">
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Omnis odio velit
    ullam quas maiores voluptas sed quae quibusdam dolore sapiente id nobis,
    impedit eum facere incidunt optio magnam laboriosam quo.
  </p>
</template>

<script>
export default {
  data() {
    return {
      isHome: true,
      pClass: ["text", "text-home"],
      classVar: "title",
      styleClass: {
        color: "aqua",
        backgroundColor: "black",
        "font-size": "20px",
      },
    };
  },
};
</script>

<style></style>
