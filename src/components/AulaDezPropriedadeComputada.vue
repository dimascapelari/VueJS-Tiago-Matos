<template>
  <div>
    {{ user.first_name }} {{ user.last_name }}
    <br />
    {{ fullName }}
    <br />
    <!-- --------------- -->
    <br />

    <h2>Todos em aberto</h2>
    <div v-for="(todo, index) in naoCompletadas" :key="index">
      {{ todo.title }}
      <span>
        <b> {{ todo.completed }}</b>
      </span>
    </div>

    <h2>Todos completas</h2>
    <div v-for="(todo, index) in completadas" :key="index">
      {{ todo.title }}
      <span>
        <b>{{ todo.completed }}</b>
      </span>
    </div>

    <br />
    <br />
    <h2>Todos</h2>
    <div v-for="(todo, index) in todos" :key="index">
      <input v-model="todo.completed" type="checkbox" />

      {{ todo.title }}
    </div>
  </div>
</template>

<script>
export default {
  name: "AulaDezPropriedadeComputada",
  data() {
    return {
      user: {
        first_name: "Dimas",
        last_name: "Capelari",
      },
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
  computed: {
    fullName() {
      return `${this.user.first_name} ${this.user.last_name} `;
    },

    naoCompletadas() {
      return this.todos.filter((todo) => !todo.completed);
    },
    completadas() {
      return this.todos.filter((todo) => todo.completed);
    },
  },
};
</script>

<style></style>
