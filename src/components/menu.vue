<template>
  <el-container>

    <el-input v-model="input1" placeholder="请输入内容"></el-input>
    <el-input v-model="input2" placeholder="请输入内容"></el-input>
    <el-button type="primary" v-on:click="hello">主要按钮</el-button>

  </el-container>

</template>

<script>
export default {
  name: 'amenu',
  data () {
    return {
      input1: 120,
      input2: 30
    }
  },
  methods: {
    hello: function () {
      this.$emit('added', this.input1, this.input2)
    }
  }
}
</script>

<style>
</style>
