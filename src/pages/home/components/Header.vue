<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
      </div>
    <div class="header-right">
      城市
      <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader'
}
</script>

<style scoped>
  .header{
    display: flex;
    height: .86rem;
    background: #00bcd4;
    line-height: .86rem;
    color: #fff;
  }
  .header-left{
    width: .86rem;
    float: left;
  }
  .header-right{
    width: 1.42rem;
    float: right;
    text-align: center;
  }
  .header-input{
    flex: 1;
    background: #fff;
    border-radius: .1rem;
    margin: .12rem .1rem;
    height: .64rem;
    line-height: .64rem;
    padding-left: .2rem;
    color: #ccc;
  }
  .back-icon{
    text-align: center;
  }
  .arrow-icon{
    font-size: .26rem;
  }
</style>
