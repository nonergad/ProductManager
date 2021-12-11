<template>
  <div class="Container">
    <ItemInput :placeholder-text="namePlaceholder"></ItemInput>
    <ItemInput :placeholder-text="imagePlaceholder"></ItemInput>
    <DescriptionInput :placeholder-text="descriptionPlaceholder"></DescriptionInput>
    <ItemInput :placeholder-text="pricePlaceholder"></ItemInput>
    <AddButton></AddButton>
  </div>
</template>

<script>
import AddButton from "@/components/AddButton";
import DescriptionInput from "@/components/DescriptionInput";
import ItemInput from "@/components/ItemInput";
export default {
  name: "InputContainer",
  components: {ItemInput, DescriptionInput,AddButton},
  data() {
    return {
      namePlaceholder: "Введите наименование товара",
      descriptionPlaceholder: "Введите описание товара",
      imagePlaceholder: "Введите ссылку",
      pricePlaceholder: "Введите цену"
    }
  }

}
</script>

<style scoped>
  .Container{
    width: 332px;
    height: 440px;
    padding: 24px;
    background-color: #42b983;
    box-sizing: border-box;
  }
</style>