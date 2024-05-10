<template>
  <div>
    {{ fullName }}
  </div>
  
  <br><br>

  <div
    v-for="todo in todos"
    :key="todo.id"
  >
    {{ todo.title }} <span>{{ todo.completed }}</span>
  </div>

</template>

<script>

export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      user: {
        first_name: 'Jon',
        last_name: 'Snow',
      },
      todos: [
      {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false,
          "imgSrc": "https://via.placeholder.com/150"
      },
      {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false,
          "imgSrc": "https://via.placeholder.com/150"
      },
      {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
      },
      {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
      },
      {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
      }]
    }
  },

  computed: {
    fullName() {
      return `${this.user.first_name} ${this.user.last_name}`
   },
  },

  methods: {
    click() {
      console.log(this.user)
    }
  }
}
</script>

<style>

#app {
  font-family: Avenir, Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}

</style>
