<template>
  <div class="Container">
    <RequiredText :flag="true" :text="productText"></RequiredText>
    <ItemInput :placeholder-text="namePlaceholder"></ItemInput>
    <RequiredText :flag="false" :text="descriptionText"></RequiredText>
    <DescriptionInput :placeholder-text="descriptionPlaceholder"></DescriptionInput>
    <RequiredText :flag="true" :text="imageText"></RequiredText>
    <ItemInput :placeholder-text="imagePlaceholder"></ItemInput>
    <RequiredText :flag="true" :text="priceText"></RequiredText>
    <ItemInput :placeholder-text="pricePlaceholder"></ItemInput>
    <AddButton></AddButton>
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
    }
  }

}
</script>

<style scoped>
  .Container{
    width: 332px;
    height: 440px;
    padding: 24px;
    box-sizing: border-box;
    background: #FFFEFB;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
  }
</style>