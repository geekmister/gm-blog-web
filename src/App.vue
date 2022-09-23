<template>
  <Title></Title>
  <div class="main-container">
    <Nav></Nav>
    <router-view></router-view>
  </div>
</template>

<script>
import Title from "./components/base/Title.vue";
import Nav from "./components/base/Nav.vue";
import {defineComponent} from "vue";

export default defineComponent({
  components: {Title, Nav}
})
</script>

<!--
  KNOWN: scoped的定义和作用
  定义：
  在Vue文件中的style标签上有一个特殊的属性，scoped。当一个style标签拥有scoped属性时候，它的css样式只能用于当前的Vue组件，
  可以使组件的样式不相互污染。如果一个项目的所有style标签都加上了scoped属性，相当于实现了样式的模块化。
  参考指南：https://blog.csdn.net/sinat_17775997/article/details/83416617
-->
<style>
.main-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: flex-start;
  width: 100%;
  height: 100%;
}
</style>
