<template>
  <div class="ProductContainer">
    <Product class="productItem" :key="index" v-for="(item, index) in allProducts" :product="item"></Product>
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
    allProducts: Array
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