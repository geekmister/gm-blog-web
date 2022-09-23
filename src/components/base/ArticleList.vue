<template>
  <div class="container">
    <template v-for="item in items">
      <div class="item-container">
        <img class="item-img" src="../../assets/img/sample/sample-2.png"/>
        <div class="item-info-container">
          <span class="item-info-title">{{item.title}}</span>
          <span class="item-info-abstract">{{item.abstract}}</span>
          <div class="item-info-label-container">
            <img class="item-info-label-icon" src="../../assets/icon/time@2x.png"/>
            <span style="margin-left: 5px">{{item.time}}</span>
            <img class="item-info-label-icon" style="margin-left: 20px" src="../../assets/icon/special-column@2x.png"/>
            <span style="margin-left: 5px">{{item.sc}}</span>
          </div>
        </div>
      </div>
    </template>
  </div>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "ArticleList",
  setup() {
    const items = [
      {zoom: "", title: "为生活再种下一颗种子", abstract: "如果 10年前，我一心 “坚持” 下去了汽车装潢，可能我现在会是一家装潢店的老板，也许是连锁店，也许是一家…", time: "两天前", sc: "生活杂事"},
      {zoom: "", title: "为生活再种下一颗种子", abstract: "如果 10年前，我一心 “坚持” 下去了汽车装潢，可能我现在会是一家装潢店的老板，也许是连锁店，也许是一家…", time: "两天前", sc: "生活杂事"}
    ]

    return {
      items
    }
  }
})
</script>

<style scoped>
.container {
  margin-left: 20px;
  margin-top: 10px;
}
.item-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  width: 650px;
  height: 140px;
  border: 1px solid #F0F0F2;
  border-radius: 10px;
  margin-top: 10px;
  padding-left: 20px;
  padding-right: 20px;
}
.item-img {
  width: 235px;
  height: 100px;
}
.item-info-container {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  margin-left: 20px;
}
.item-info-title {
  width: 160px;
  height: 22px;
  font-family: PingFangSC-Semibold;
  font-weight: 600;
  font-size: 16px;
  color: #000000;
  letter-spacing: 0;
}
.item-info-abstract {
  font-family: PingFangSC-Regular;
  font-weight: 400;
  font-size: 14px;
  color: #333333;
  letter-spacing: 0;
  margin-top: 8px;
}
.item-info-label-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  margin-top: 12px;
}
.item-info-label-icon {
  width: 17px;
  height: 17px;
}
</style>