<template>
  <input class="inputs" :placeholder="placeholderText">
</template>

<script>
export default {
  name: "ItemInput",
  props:{
    placeholderText: String
  }
}


</script>

<style scoped>
  .inputs{
    width: 100%;
    height: 36px;
    background-color: red;
    box-sizing: border-box;
  }
</style>