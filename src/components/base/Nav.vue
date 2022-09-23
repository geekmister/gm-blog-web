<template>
  <div class="container">
    <template v-for="item in items">
      <div :class="item.clicked ? 'item-container-light' : 'item-container-dark'">
        <img class="item-img" src="../../assets/img/sample/sample-1.png"/>
        <span :class="item.clicked ? 'item-name-light' : 'item-name-dark'">{{item.name}}</span>
      </div>
    </template>
  </div>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "Nav",
  setup() {
    const items = [
      {img: "../../assets/img/sample/sample-1.png",  name: "首页", clicked: true},
      {img: "../../assets/img/sample/sample-1.png",  name: "生活杂事", clicked: false}
    ]

    return {
      items
    }
  }
})
</script>

<style scoped>
.container {
  margin-left: 90px;
  margin-top: 20px;
}
.item-container-light {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  padding-left: 10px;
  width: 285px;
  height: 50px;
  background: #EA6F5A;
  border-radius: 25px;
  margin-bottom: 10px;
}
.item-container-dark {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  padding-left: 10px;
  width: 285px;
  height: 50px;
  background: #FFFFFF;
  border-radius: 25px;
  margin-bottom: 10px;
}
.item-img {
  width: 35px;
  height: 35px;
}
.item-name-light {
  font-family: PingFangSC-Semibold;
  font-weight: 600;
  font-size: 16px;
  color: #FFFFFF;
  letter-spacing: 0;
  margin-left: 10px;
}
.item-name-dark {
  font-family: PingFangSC-Semibold;
  font-weight: 600;
  font-size: 16px;
  color: #000000;
  letter-spacing: 0;
  margin-left: 10px;
}

</style>