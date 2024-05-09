<template>
  <div>

    <button @click.once="onClick">
      Enviar
    </button>

    <br><br>

    <div @mouseover="onMouseOver"
        @mouseout="onMouseOut()" 
    >
      Mouse over
    </div>

    <br><br>

    <form
      action="https://google.com"
      v-on:submit.prevent="onSubmit"
    >
      <input 
        type="text"
        @keyup.enter="onKeyUp"
      >
      <button type=submit>
        Enviar
      </button>
    </form>
    
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      
    }
  },

  methods: {
    onClick($evt) {
      console.log('click', $evt)
    },
    onMouseOver($evt) {
      console.log('mouse over', $evt)
    },
    onMouseOut() {
      console.log('mouse out')
    },
    onSubmit() {
      console.log('submit')
    },
    onKeyUp($evt) {
      console.log('onKeyUp', $evt)
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
