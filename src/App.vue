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

  <TheHeader v-if="showHeader" />

  <hr />

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

  <h3>V-for</h3>
  <div>
    <div class="todos-item" v-for="(obj, index) in todos" :key="index">
      <img v-if="obj.imgSrc" :src="obj.imgSrc" />
      {{ index }} - {{ obj.title }}
    </div>
  </div>

  <hr />

  <div></div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";

export default {
  name: "App",
  components: {
    TheHeader,
  },
  data() {
    return {
      isHome: true,
      classVar: "title",
      showHeader: true,
      firstName: "Dimas",
      lastName: "Capelari",
      showName: true,
      accessLevel: "marketing",
      // imgAlt: "Foto Teste",
      styleClass: {
        color: "aqua",
        backgroundColor: "black",
        "font-size": "20px",
      },
      pClass: ["text", "text-home"],
      todos: [
        {
          userId: 1,
          id: 1,
          title: "delectus aut autem",
          completed: false,
          imgSrc: "https://via.placeholder.com/150",
        },
        {
          userId: 1,
          id: 2,
          title: "quis ut nam facilis et officia qui",
          completed: false,
          imgSrc: "https://via.placeholder.com/150",
        },
        {
          userId: 1,
          id: 3,
          title: "fugiat veniam minus",
          completed: false,
        },
        {
          userId: 1,
          id: 4,
          title: "et porro tempora",
          completed: true,
        },
        {
          userId: 1,
          id: 5,
          title:
            "laboriosam mollitia et enim quasi adipisci quia provident illum",
          completed: false,
        },
      ],
    };
  },
};
</script>

<style>
.title {
  font-size: 20px;
  color: blue;
}

.title-home {
  font-size: 40px;
  color: green;
}

.text {
  color: red;
}

.text-home {
  color: greenyellow;
}

.todos-item {
  background: #000;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #fff;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
