<template>
  <div id="app">
    <input v-model.number="num1" type="number" />        
    <span>+</span>
    <input v-model.number="num2" type="number" />
    <span>=</span>
    <span>{{num1 + num2}}</span>
    <br>
    <select name="food" v-model='name'>
      <option>taco</option>
      <option>burrito</option>
    </select>
    <span v-if="name">My favorite food is {{name}}</span>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// new Vue({
//   el: '#app',
//   data(){
//     return{
//       num1: 0,
//       num2: 0,
//       name: ''
//     }
//   }
// })
export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data(){
    return{
      num1: 0,
      num2: 0,
      name: ''
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
