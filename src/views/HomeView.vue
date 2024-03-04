<template>
  <div class="content">
    <!-- 顶部容器
		<dv-top-container>顶部容器</dv-top-container>
		侧边容器
		<dv-side-container>侧边容器</dv-side-container>
		侧边容器
		<dv-bottom-container>侧边容器</dv-bottom-container>
		侧边容器
		<dv-footer-container>侧边容器</dv-footer-container> -->
    <!-- 全屏容器 -->
    <dv-full-screen-container>
      <moduleTitle />
      <moduleMain />
      <moduleThird />
    </dv-full-screen-container>
  </div>
</template>

<script>
import moduleMain from "./moduleMain.vue";
import moduleTitle from "./moduleTitle.vue";
import moduleThird from "./moduleThird.vue";

export default {
  name: "HomeView",
  components: {
    moduleTitle,
    moduleMain,
    moduleThird,
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
.content {
  color: #fff;
  background: url("../assets/img/pageBg.png") no-repeat center center;
  background-size: cover;
  width: 100%;
  height: 100vh;
}

.module-box {
  display: flex;
  justify-content: space-between;
  margin: 10px;
}
</style>
