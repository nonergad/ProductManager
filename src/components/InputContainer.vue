<template>
  <div class="containerWrapper">
    <form class="Container" >
      <RequiredText :flag="true" :text="productText"></RequiredText>
      <input class="inputs" :class="!productInfo.productName && 'inpRed'" :placeholder="namePlaceholder" required v-model="productInfo.productName"/>
      <RequiredText :flag="false" :text="descriptionText"></RequiredText>
      <textarea class="Description" :placeholder="descriptionPlaceholder" v-model="productInfo.description"/>
      <RequiredText :flag="true" :text="imageText"></RequiredText>
      <input class="inputs" :class="!productInfo.imgUrl && 'inpRed'" :placeholder="imagePlaceholder" required v-model="productInfo.imgUrl"/>
      <RequiredText :flag="true" :text="priceText"></RequiredText>
      <input class="inputs" :class="!productInfo.price && 'inpRed'" type="number" :placeholder="pricePlaceholder" required v-model="productInfo.price"/>
      <AddButton :class="productInfo.productName && productInfo.imgUrl && productInfo.price && 'btnGreen'" :func="deploy"></AddButton>
    </form>
  </div>

</template>

<script>
import RequiredText from "@/components/RequiredText";
import AddButton from "@/components/AddButton";
export default {
  name: "InputContainer",
  components: {AddButton, RequiredText},
  data() {
    return {
      namePlaceholder: "Введите наименование товара",
      descriptionPlaceholder: "Введите описание товара",
      imagePlaceholder: "Введите ссылку",
      pricePlaceholder: "Введите цену",
      productText: "Наименование товара",
      descriptionText:"Описание товара",
      imageText:"Ссылка на изображение товара",
      priceText: "Цена товара",
      isActive: true,
      productInfo:{
        productName: '',
        description:'',
        imgUrl:'',
        price:''
      }
    }
  },
  methods:{
    deploy(event){
      event.preventDefault()
      if(this.productInfo.productName && this.productInfo.imgUrl && this.productInfo.price){
        this.$emit('product', {product: this.productInfo})
      }
    }
  }

}
</script>

<style scoped>
  .containerWrapper{
    position: relative;
    width: 332px;
    height: 1000px;
  }

  .Container{
    position: fixed;
    width: 332px;
    height: 440px;
    padding: 24px;
    box-sizing: border-box;
    background: #FFFEFB;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
  }

  .inpRed{
    border:2px solid red;
  }

  .btnGreen{
    color: #FFFFFF;
    background: #7BAE73;
  }

  input{
    border: 0px none;
  }
  .inputs{
    width: 100%;
    height: 36px;
    box-sizing: border-box;
    background: #FFFEFB;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;
    font-family: Source Sans Pro;
    font-weight: 400;
    font-size: 12px;
    line-height: 15px;
  }

  .Description{
    width: 100%;
    height: 108px;
    box-sizing: border-box;
    background: #FFFEFB;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;
    font-family: 'Source Sans Pro', sans-serif;
    font-weight: normal;
    font-size: 12px;
    line-height: 15px;
    resize: none;
  }
</style>