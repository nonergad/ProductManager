<template>
  <div class="ProductContainer">
  <button></button>
    <div class="img"></div>
    <div class="ProductInfo">
      <h2 class="ProductName">Наименование товара</h2>
      <span>Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк</span>
      <h2>10 000 руб.</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "Product"
}
</script>

<style scoped>
  h2{
    margin: 0px;
  }
  p{
    margin: 0px;
  }
  .ProductContainer{
    width: 332px;
    height: 423px;
    background: #FFFEFB;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;

  }

  .img{
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
</style>