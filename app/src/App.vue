<template>

  <p class=card>Teste</p>
  
  <div>
    <BaseCard></BaseCard>
  </div>

</template>

<script>
import BaseCard from '@/components/BaseCard.vue';

export default {
  name: 'App',
  components: {
    BaseCard
  },
  data() {
    return {
      
    }
  },

  computed: {

  },

  methods: {

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
