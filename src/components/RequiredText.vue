<template>
  <div class="TextContainer">
    <label class="Text">{{text}}</label>
    <div v-if="flag" class="Redpoint"></div>
  </div>
</template>

<script>
export default {
  name: "RequiredText",
  props:{
    flag: Boolean,
    text: String
  }
}
</script>

<style scoped>
  .TextContainer{
    display: flex;
    margin-top: 16px;
  }

  .Redpoint{
    width: 4px;
    height: 4px;
    background: #FF8484;
    border-radius: 4px;
  }

  .Text{
    margin: 0px;
    font-family: Source Sans Pro;
    font-weight: 400px;
    font-size: 10px;
    line-height: 13px;
    letter-spacing: -0.02em;
    color: #49485E;
  }
</style>