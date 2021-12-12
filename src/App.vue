<template>
  <div id="app">
    <div>
      <Header></Header>
      <div class="main">
        <InputContainer></InputContainer>
        <ProductsContainer></ProductsContainer>
      </div>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import InputContainer from './components/InputContainer';
import ProductsContainer from "@/components/ProductsContainer";
import Header from "@/components/Header";
export default {
  name: 'App',
  components: {
    InputContainer,
    ProductsContainer,
    Header
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
@import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@400;600&display=swap');
#app {
  font-family: 'Source Sans Pro', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-top: 50px;
  display: flex;
  justify-content: space-between;
  background: rgba(240, 240, 240, 0.8);
}

.main{
  display: flex;
  flex-direction: row;
}
</style>
