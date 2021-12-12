<template>
  <div class="HeaderContainer">
    <h1 class="HeaderText">Добавление товара</h1>
    <SortList></SortList>
  </div>
</template>

<script>
import SortList from "@/components/SortList";
export default {
  name: "Header",
  components:{SortList}
}
</script>

<style scoped>
  .HeaderContainer{
    margin: 32px 0px 16px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .HeaderText{
    margin: 0px;
    font-weight: 600;
    font-size: 28px;
    line-height: 35px;
    color: #3F3F3F;
  }
</style>