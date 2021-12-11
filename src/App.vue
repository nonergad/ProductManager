<template>
  <div id="app">
    <InputContainer></InputContainer>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import InputContainer from './components/InputContainer'
export default {
  name: 'App',
  components: {
    InputContainer
  },
  data() {
    return {
      data: 0
    }
  },
  methods:{
    clickHandler(){
      console.log(1)
      this.data++
    }
  },
  created(){

  },
  mounted(){

  },
  updated() {
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
