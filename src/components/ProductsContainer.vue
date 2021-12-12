<template>
  <div class="ProductContainer">
    <Product></Product>
    <Product></Product>
    <Product></Product>
    <Product></Product>
    <Product></Product>
    <Product></Product>
  </div>
</template>

<script>
import Product from "@/components/Product";
export default {
  name: "ProductsContainer",
  components:{
    Product
  },
  props:{
    Product:[]
  }
}
</script>

<style scoped>
  .ProductContainer{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 1028px;
  }
</style>