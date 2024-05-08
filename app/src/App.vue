<template>
  <!--<TheHeader
    v-if="showHeader"
  />

  <div v-show="showName">
    Nome: {{ firstName }} <br>
    Sobrenome: {{ lastName }}
  </div>

  <div v-if="accessLevel === 'admin'">Usuário Admin</div>
  <div v-else-if="accessLevel === 'marketing'">Usuário Marketing</div>
  <div v-else>Usuário normal</div>-->

  <div>

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
//import HelloWorld from './components/HelloWorld.vue'
//import TheHeader from './components/TheHeader'

export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      showHeader: true,
      firstName: 'Jon',
      lastName: 'Snow',
      showName: false,
      accessLevel: 'admin',
      
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
      }
    ]
      
    }
  }
}
</script>

<style>
.todos-item {
  background: #000;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #ffff;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}
</style>
