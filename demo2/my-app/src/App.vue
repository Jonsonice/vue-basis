<template>
  <div id="app">
    {{msg}}
    <div>
      <input type="text" v-model="info">
      <button @click="handleClick">添加</button>
    </div>
    <ul>
      <todo-item v-for="item in list" :key="item">
        <template v-slot:item="itemProps">
          <span :style="{fontSize:'20px',color:itemProps.checked ? 'brown': 'blue'}">{{item}}</span>
        </template>
      </todo-item>

      <!-- <todo-item v-for="item in list" :key="item">
          <span style="font-size:20px" slot="item">{{item}}</span>
      </todo-item> -->
      <!-- 不同写法 -->

    </ul>
  </div>
</template>

<script>
import TodoItem from './components/TodoItem'

export default {
  name: 'app',
  data () {
    return {
      msg: 'hello msg',
      info: '',
      list: [],
    }
  },
  methods: {
    handleClick(){
      // console.log(this.info)
      this.list.push(this.info)
      this.info = ''
    }
  },
  components: {
    TodoItem
  }
}
</script>
 
<style>

</style>
