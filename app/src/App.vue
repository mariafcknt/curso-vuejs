<template>
  
  <div>

    <TheHeader>
      
      <template v-slot:description>
        <p>Description</p>
      </template>

      Lorem ipsum dolor sit amet consectetur adipisicing elit.

    </TheHeader>

    

  </div>

</template>

<script>
import TheHeader from '@/components/TheHeader.vue';

export default {
  name: 'App',
  components: {
    TheHeader
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
