<template>
  <input class="Description" :placeholder="placeholderText">
</template>

<script>
export default {
  name: "DescriptionInput",
  props: {
    placeholderText: String
  }
}
</script>

<style scoped>
  input{
    border: 0px none;
  }

  .Description{
    width: 100%;
    height: 108px;
    box-sizing: border-box;
    background: #FFFEFB;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;
    font-weight: normal;
    font-size: 12px;
    line-height: 15px;
    color: #B4B4B4;
  }
</style>