<template>

  <div>

    <h1 :class="{ 'title': true, 'title-home': isHome }">Curso Vue 3</h1>

    <p :class="pClass">
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Unde ducimus, harum magni blanditiis amet et iste facilis atque culpa voluptatem itaque quis magnam numquam nobis ipsum quia molestias doloremque temporibus?
    </p>

    <p :style="{'color': 'cadetblue', 'background-color': 'black'}">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Inventore totam iusto ipsa, asperiores corporis error, sunt neque, cupiditate possimus magnam hic voluptates atque! Sed quae explicabo nesciunt ipsam non est?
    </p>

    <div
      v-for="(obj, index) in todos"
      :key="obj.id"
      class="todos-item"
    > 
      <img
      v-if="obj.imgSrc"
      v-bind:src="obj.imgSrc">
      {{ index + 1}} - {{ obj.title }}
    </div>

  </div>

</template>

<script>

export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      showHeader: true,
      classVar: 'title',
      pClass: ['text', 'text-home'],
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
  }
}
</script>

<style>
.title {
  font-size: 20px;
  color: blue;
}

.title-home {
  font-size : 40px;
  color: green;
}

.text {
  color: #14a094;
}

.text-home {
  color: purple;
}

.todos-item {
  background: #000;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #ffff;
}

#app {
  font-family: Avenir, Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}
</style>
