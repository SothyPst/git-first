
<template>
  <div id="app" class="body">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <page1 msg="Page1 ......."> </page1>
    <p>result: {{result}}</p>
    <p>watch result: {{changeResult}}</p>
    <button @click="sum">sum</button>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Page1 from "./Page1.vue";
export default {
  name: "app",
  components: {
    HelloWorld,
    Page1
  },
  data() {
    return {
      value1: 10,
      value2: 10,
      result: 0,
      changeResult: 'not changed'
    };
  },
  methods: {
    sum() {
      this.result = this.value1 + this.value2;
    }
  },
  watch: {
    result(newValue){
      this.changeResult = "changed"
    }
  }

};
</script>
 
<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
