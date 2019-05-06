<template>
    <div>
     <h1>
       Hello Info!!!
     </h1>
      <button type="type" @click="add()">添加</button>
    </div>
</template>

<script>

import store from '@/store.js'
export default {
  name: 'Info',
  comments: {
    store
  },
  methods: {
    add: function () {
      console.log('This is Info')
      store.commit('increat')
    }
  }
}
</script>

<style scoped>

</style>
