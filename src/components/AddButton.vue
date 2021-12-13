<template>
  <button v-bind:class="{isActive:ActiveBtn}" class="AddBtn" @click="(event) => func(event)" >Добавить</button>
</template>

<script>
export default {
  name: "AddButton",
  props:{
    isActive: Boolean,
    func: Function
  }
}
</script>

<style scoped>

  button{
    border: 0px none;
  }

  .AddBtn{
    box-sizing: border-box;
    margin-top: 24px;
    width: 100%;
    height: 36px;
    background: #EEEEEE;
    border-radius: 10px;
  }

</style>