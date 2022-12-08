<template>
  <div>
    <div class="todos-item" v-for="(obj, index) in todos" :key="index">
      <img v-if="obj.imgSrc" :src="obj.imgSrc" />
      {{ index }} - {{ obj.title }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
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

<style></style>
