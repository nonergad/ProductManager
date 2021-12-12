<template>
  <button v-bind:class="{isActive:ActiveBtn}" class="AddBtn">Добавить</button>
</template>

<script>
export default {
  name: "AddButton",
  props:{
    isActive: Boolean
  }
}
</script>

<style scoped>

  button{
    border: 0px none;
  }

  .AddBtn{
    margin-top: 24px;
    width: 100%;
    height: 36px;
    background: #EEEEEE;
    border-radius: 10px;
    border-color: none;
  }

  .ActiveBtn{
    background: #7BAE73;
  }
</style>