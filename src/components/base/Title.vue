<template>
  <div class="container">
    <div class="logo-container">
      <img class="logo-img" src="../../assets/img/geekmister-head@2x.png">
      <div class="logo-desc">
        <span class="logo-desc-title">极客先生</span>
        <span class="logo-desc-desc">程序员 | 创业者 | 自媒体 | 白帽子</span>
      </div>
    </div>
    <span class="title">爱自由，爱生活！</span>
  </div>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "title",
  setup() {},
})
</script>

<style scoped>
.container {
  width: 100%;
  height: 58px;
  background-color: #FFFFFF;
  text-align: center;
  padding-left: 20px;
  padding-right: 20px;
  border-bottom: 1px solid #F5F5F7;
}
.title {
  width: 160px;
  height: 25px;
  font-family: PingFangSC-Semibold;
  font-weight: 600;
  font-size: 18px;
  color: #000000;
  letter-spacing: 2px;
  line-height: 58px;
  position: relative;
  left: -112px;
}
/* TODO: 没搞懂calc */
.logo-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  float: left;
  position: relative;
  top: calc(50% - 20px)
}
.logo-img {
  width: 40px;
  height: 40px;
}
.logo-desc {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  margin-left: 10px;
}
.logo-desc-title {
  width: 80px;
  height: 25px;
  font-family: PingFangSC-Semibold;
  font-weight: 600;
  font-size: 18px;
  color: #000000;
  letter-spacing: 2px;
}
.logo-desc-desc {
  width: 175px;
  height: 17px;
  font-family: PingFangSC-Regular;
  font-weight: 400;
  font-size: 12px;
  color: #000000;
  letter-spacing: 0;
}
</style>