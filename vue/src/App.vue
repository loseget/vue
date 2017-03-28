<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1 v-text="title"></h1>
    <ul>
      <li v-for="item in items" v-bind:class="{finished:item.isFinished}" @click="toggleFinish(item)">
        {{item.lable}}
      </li>
    </ul>
  </div>
</template>

<script>
  import Hello from './components/Hello'
  //什么时候
  export default {
    data: function() {
      return {
        title: 'it is my life!',
        items: [{
            lable: '开始制作游戏',
            isFinished: false
          },
  
          {
            lable: '开始弹弹Ukelele',
            isFinished: false
          },
  
          {
            lable: '开始学习心理学',
            isFinished: false
          }
  
        ]
      }
    },
    methods: {
  
      toggleFinish: function(item) {
        console.log(item)
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
