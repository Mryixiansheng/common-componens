<template>
    <div class="index">
      <div class="list wrap">
        <button v-for="(item, index) in $router.options.routes" :key="index" @click="$router.push(item.path)" v-show="item.show">{{item.chineseName}} {{item.integrity}}%</button>
      </div>
    </div>
</template>

<script type="text/ecmascript-6">
export default {
  data () {
    return {
    }
  },
  mounted () {
    console.log(this.$router)
  }
}
</script>

<style lang="less" scoped>
.list{
  display: flex;
  flex-wrap: wrap;
  button{
    height: 30px;
    padding: 0 20px;
    border: 1px solid #ccc;
    line-height: 30px;
    background-color: #fff;
    border-radius: 5px;
    cursor: pointer;
    margin: 20px;
  }
}
</style>
