<template>
  <div class="ProductContainer">
    <div v-if="activeProduct" class="delBtnContainer">
      <button class="delBtn"></button>
    </div>
    <div class="img"></div>
    <div class="ProductInfo">
      <h2 class="ProductName">Наименование товара</h2>
      <p class="ProductText">Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк</p>
      <h2 class="ProductPrice">10 000 руб.</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "Product",
  props:{
    product:{}
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
    margin: 0px;
  }
  p{
    margin: 0px;
  }

  .ProductName{
    font-weight: 600;
    font-size: 20px;
    line-height: 25px;
  }

  .ProductContainer{
    position: relative;
    width: 332px;
    height: 423px;
    background: #FFFEFB;
    color: #3F3F3F;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;

  }

  .img{
    box-sizing: border-box;
    width: 100%;
    height: 200px;
    background: url("img.png") no-repeat center/contain;
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