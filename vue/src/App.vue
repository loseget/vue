<template>
  <div id="app">
    <div>
    <img src="./assets/logo.png">
    <h1 v-text="title"></h1>
    <ul>
      <li v-for="item in items"
          v-bind:class="{finished:item.isFinished}"
          @click="toggleFinish(item)">
        {{item.lable}}
      </li>
    </ul>
    </div>
    <div>
      <el-button @click="visible = true"  type="info">按钮</el-button>
      <el-dialog v-model="visible"
                 title="Hello world">
        <p>欢迎使用 Element</p>
      </el-dialog>
      <el-alert title="成功提示的文案"
                type="success">
      </el-alert>
      <el-alert title="消息提示的文案"
                type="info">
      </el-alert>
      <el-alert title="警告提示的文案"
                type="warning">
      </el-alert>
      <el-alert title="错误提示的文案"
                type="error">
      </el-alert>
    </div>
  </div>
</template>

<script>
import Hello from './components/Hello'
//什么时候
export default {
  data: function () {
    return {
      title: 'it is my life!',
      visible :false,
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

    toggleFinish: function (item) {
      console.log(item)
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>