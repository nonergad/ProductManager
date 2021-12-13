<template>
  <input class="inputs" :placeholder="placeholderText" required @input="(event) => this.$emit('input', event.target.value)">
</template>

<script>
export default {
  name: "ItemInput",
  props:{
    placeholderText: String
  },
  data() {
    return {
      text: ''
    }
  },
  methods:{
    saveInfo() {

    }
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
  font-family: Source Sans Pro;
  font-weight: 400;
  font-size: 12px;
  line-height: 15px;
}
</style>