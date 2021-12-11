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
  }
</style>