<template>

  <TheHeader v-if="showHeader"/>
  
  <div>
    <h1>Hello World</h1>
    <br>
    <input 
      v-model="name"
      type="text"
    >
    {{ name }}

    <br>

    <button @click="toggleHeader">
      Ativar e desativar header
    </button>
  </div>

</template>

<script>

import TheHeader from './components/TheHeader.vue';

export default {
  name: 'App',
  components: {
    TheHeader
  },
  data() {
    return {
      name: 'Jon Snow',
      showHeader: true,
    }
  },

  beforeUpdate() {
    console.log('beforeUpdate');
  },
  updated() {
    console.log('updated');
  },
  /* beforeCreate(){
    console.log("beforeCreate");
    console.log('Estado: ', this.name);
    console.log('DOM: ', this.$el);
  },
  created() {
    console.log("created");
    console.log('Estado: ', this.name);
    console.log('DOM: ', this.$el);
  },
  beforeMount() {
    console.log("beforeMount");
    console.log('Estado: ', this.name);
    console.log('DOM: ', this.$el);
  },
  mounted() {
    console.log("mounted");
    console.log(this.name);
    console.log('DOM: ', this.$el);
  },
  beforeUnmount() {
    console.log("beforeUnmount");
  },
  unmounted() {
    console.log("unmounted");
  }, */

  watch: {

  },

  computed: {

  },

  methods: {
    toggleHeader() {
      this.showHeader = !this.showHeader
    },
    deactivateHeader() {
      this.showHeader = false;
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
