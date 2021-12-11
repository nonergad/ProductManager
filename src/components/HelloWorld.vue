<template>
  <div>
    <div @click="()=> {this.$emit('new-event')}">кнопка</div>
    <div>{{data}}</div>
    <p v-for="elem in arr" :key="elem">{{elem}}</p>
    <button @click="clickHandler">жми</button>
    <div v-if="flag">Хер</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      arr: ['popka', 'alexey', 'pivo'],
      flag: false
    }
  },
  props: {
    msg: String,
    number: Number,
    data:Number
  },
  methods:{
    clickHandler() {
      this.flag = !this.flag
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
