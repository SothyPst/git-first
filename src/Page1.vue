<template>
  <div>
    <h1>Hello World {{a+b}}</h1>
    <h1>{{ msg }}</h1>
    <button @click="sum" >Get Result  As Total : {{c}}</button> 
    <h1 v-if="name">{{name}}</h1>
    <input v-model="name"/>
  </div>
</template>
<script>
export default {
  name: "Page1",
  props: {
    msg: String
  },
  data(){

    return{
      a: 2,
      b: 3,
      c:'',
      name: ''
    };
  },
  methods: {
    sum() {
      this.c = this.a + this.b;
    }
  },
  watch: {
    name(nextValue){
console.log('name is changed')
    }
  }
};
</script>

<style>
</style>

