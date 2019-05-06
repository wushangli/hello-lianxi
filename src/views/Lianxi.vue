<template>
  <div>
    <ul>
      <li v-for="(item,index) in showList"
          @click="choose(index)"
          :class="{activity: index==current && current !== '' }"
          :key="index"
          >
        {{item}}
      </li>
    </ul>
    <button type="button" @click="add()">添加</button>
    <ul>
      <li v-for="(item,index) in targetList" :key="index">{{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Lianxi',
  data: function () {
    return {
      current: '',
      showList: [1, 2, 3, 4, 5, 6, 7, 8],
      targetList: []
    }
  },
  methods: {
    choose (index) {
      this.current = index
      console.log(this.current)
    },
    add () {
      if (this.current === '') return
      this.targetList.push(this.showList[this.current])
      this.current = ''
    }
  }
}
</script>

<style scoped>
    .activity{
      background: greenyellow;
    }
</style>
