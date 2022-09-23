<template>
  <div class="container">
    <div class="sign-container">
      <div class="sign-item-container">
        <img class="sign-label-icon" src="../../assets/icon/time@2x.png" />
        <span class="sign-item-text">{{items[0].text}}</span>
      </div>
      <div class="sign-item-container">
        <img class="sign-label-icon" src="../../assets/icon/copyright@2x.png" />
        <span class="sign-item-text">{{items[1].text}}</span>
      </div>
    </div>
  </div>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "ArticleDetails",
  setup() {
    const items = [
      {text: "本文于 2022-7-16 11:17 由 极客先生 发布在 生活杂事 专栏"},
      {text: "版权声明：自由转载 - 署名 - 非商业性用途 - 如违规必究"}
    ]

    return {
      items
    }
  }
})
</script>

<style scoped>
.container {
  width: 650px;
  margin-left: 20px;
  margin-top: 10px;
}
.sign-container {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  width: 100%;
  height: 70px;
  border: 1px solid #F0F0F2;
  border-radius: 10px;
}
.sign-label-icon {
  width: 20px;
  height: 20px;
}
.sign-item-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  margin-top: 10px;
  margin-left: 10px;
}
.sign-item-text {
  width: 319px;
  height: 17px;
  font-family: PingFangSC-Regular;
  font-weight: 400;
  font-size: 12px;
  color: #999999;
  letter-spacing: 0;
  margin-left: 10px;
}
</style>