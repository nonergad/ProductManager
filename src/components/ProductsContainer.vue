<template>
  <div class="ProductContainer">
    <Product class="productItem"></Product>
    <Product class="productItem"></Product>
    <Product class="productItem"></Product>
    <Product class="productItem"></Product>
    <Product class="productItem"></Product>
    <Product class="productItem"></Product>
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
    margin-left: 16px;
  }

  .productItem:nth-child(3n+1){
    margin: 0;
  }
</style>