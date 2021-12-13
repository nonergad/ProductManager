<template>
  <div class="ProductInfoContainer">
    <div v-if="activeProduct" class="delBtnContainer">
      <button class="delBtn"></button>
    </div>
    <img :src="product.imgUrl" class="img"/>
    <div class="ProductInfo">
      <h2 class="ProductName">{{product.productName}}</h2>
      <p class="ProductText">{{product.description}}</p>
      <h2 class="ProductPrice">{{product.price}} руб</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "Product",
  props:{
    product: Object
  },
  data(){
    return{
      activeProduct:false
    }
  }
}
</script>

<style scoped>

  h2{
    margin: 0;
  }
  p{
    margin: 0;
  }

  .ProductName{
    font-weight: 600;
    font-size: 20px;
    line-height: 25px;
  }

  .ProductInfoContainer{
    margin: 0 0 16px 16px;
    box-sizing: border-box;
    width: 332px;
    height: 423px;
    background: #FFFEFB;
    color: #3F3F3F;
    box-shadow: 0 20px 30px rgba(0, 0, 0, 0.04), 0 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;

  }

  .img{
    box-sizing: border-box;
    width: 100%;
    height: 200px;
    border-radius: 4px 4px 0px 0px;
  }

  .ProductInfo{
    display: flex;
    flex-direction: column;
    align-items: start;
    padding: 16px 16px 24px;
    box-sizing: border-box;
  }

  .ProductText{
    margin-top: 16px;
    font-weight: 400;
    font-size: 16px;
    line-height: 20px;
    text-align: left;
    color: #3F3F3F;
  }

  .ProductPrice{
    margin-top: 32px;
    font-weight: 600;
    font-size: 24px;
    line-height: 30px;
    color: #3F3F3F;
  }

  .delBtnContainer{
    position: absolute;
    top: -8px;
    right: -8px;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 32px;
    height: 32px;
    background-color: #FF8484;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
  }

  .delBtn{
    box-sizing: border-box;
    border: 0px none;
    width: 16px;
    height: 16px;
    background: url("../img/Delete.svg") no-repeat center/ contain;
  }


</style>