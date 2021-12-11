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
  .Description{
    width: 100%;
    height: 108px;
    box-sizing: border-box;
  }
</style>