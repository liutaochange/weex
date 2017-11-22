<template>
  <div class="wrapper" @click="update">
    <div class="imgWrap">
      <image :src="logoUrl" class="logo"></image>
    </div>
    <div class="textWrap">
       <text class="Text">hello {{target}}</text>
    </div>
  </div>
</template>

<style>
  .wrapper {
    width:320px;
    flex-direction: column;
    flex-wrap: nowrap;
    justify-content: space-around;
    align-items: center;
    margin: 0 auto;
  }
  .imgWrap {
    order:1;
    flex-shrink:1;
    width: 320px;
    height: 150px;
    text-align: center;
  }
  .logo{
    width: 320px;
    height: 150px;
  }
  .textWrap{
    width: 320px;
    order: 2;
    flex-shrink:1;
    color:#888;
    font-size: 24px;
    text-align: center;
  }
  .Text{
    text-align: center;
  }
</style>

<script>
  export default {
    data: {
      logoUrl: 'http://img1.vued.vanthink.cn/vued08aa73a9ab65dcbd360ec54659ada97c.png',
      target: 'World'
    },
    methods: {
      update: function (e) {
        this.target = 'Weex'
        console.log('target:', this.target)
      }
    }
  }
</script>