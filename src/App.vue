<template>
  <div id="app">
    <h1>HOME</h1>

    <mt-header fixed title="固定在顶部"></mt-header>

    <mt-tabbar :selected.sync="selected">
      <mt-tab-item id="外卖">
        <img slot="icon" src="./assets/logo.png">
        外卖
      </mt-tab-item>
      <mt-tab-item id="订单">
        <img slot="icon" src="./assets/logo.png">
        订单
      </mt-tab-item>
      <mt-tab-item id="发现">
        <img slot="icon" src="./assets/logo.png">
        发现
      </mt-tab-item>
      <mt-tab-item id="我的">
        <img slot="icon" src="./assets/logo.png">
        我的
      </mt-tab-item>
    </mt-tabbar>

    <mt-button type="default">default</mt-button>
    <mt-button type="primary">primary</mt-button>
    <mt-button type="danger">danger</mt-button>

    <mt-radio
      title="请选择"
      v-model="value"
      :value.sync="value"
      :options="['选项A', '选项B', '选项C']">
    </mt-radio>
    <mt-cell title="标题文字"> {{ value }} </mt-cell>

    <div class="page-swipe">
      <mt-swipe :auto="4000">
        <mt-swipe-item :class="{ slide1:true }">1</mt-swipe-item>
        <mt-swipe-item :class="{ slide2:true }">2</mt-swipe-item>
        <mt-swipe-item :class="{ slide3:true }">3</mt-swipe-item>
      </mt-swipe>
    </div>

  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      selected: "外卖",
      value: ''
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}


.page-swipe .mint-swipe {
    height: 200px;
    color: #fff;
    font-size: 30px;
    text-align: center;
    margin-bottom: 20px;
}
.page-swipe .mint-swipe-item {
    line-height: 200px;
}
.page-swipe .slide1 {
    background-color: #0089dc;
    color: #fff;
}
.page-swipe .slide2 {
    background-color: #ffd705;
    color: #000;
}
.page-swipe .slide3 {
    background-color: #ff2d4b;
    color: #fff;
}
.page-swipe-desc {
    text-align: center;
    color: #666;
    margin-bottom: 5px;
}
</style>
