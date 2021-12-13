<template>
  <div class="containerWrapper">
    <div class="Container">
      <RequiredText :flag="true" :text="productText"></RequiredText>
      <ItemInput :placeholder-text="namePlaceholder" v-on:input="(event) => {console.log(event)}"/>
      <RequiredText :flag="false" :text="descriptionText"></RequiredText>
      <DescriptionInput :placeholder-text="descriptionPlaceholder"></DescriptionInput>
      <RequiredText :flag="true" :text="imageText"></RequiredText>
      <ItemInput :placeholder-text="imagePlaceholder"></ItemInput>
      <RequiredText :flag="true" :text="priceText"></RequiredText>
      <ItemInput :placeholder-text="pricePlaceholder"></ItemInput>
      <AddButton :isActive="isActive"></AddButton>
    </div>
  </div>

</template>

<script>
import RequiredText from "@/components/RequiredText";
import AddButton from "@/components/AddButton";
import DescriptionInput from "@/components/DescriptionInput";
import ItemInput from "@/components/ItemInput";
export default {
  name: "InputContainer",
  components: {ItemInput, DescriptionInput, AddButton, RequiredText},
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
        price:0
      }
    }
  }

}
</script>

<style scoped>
  .containerWrapper{
    position: relative;
    width: 332px;
    height: 440px;
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
</style>