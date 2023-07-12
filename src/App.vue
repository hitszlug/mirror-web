<script lang="ts">
import { ElContainer, ElHeader, ElFooter, ElMain, ElRow, ElCol, ElMenu, ElMenuItem, ElDivider } from 'element-plus/lib/components/index.js';
import { RouterView } from 'vue-router';
import TheHeader from './components/TheHeader/TheHeader.vue';
export default {
  components: {
    ElContainer, ElHeader, ElFooter, ElMain, ElRow, ElCol, ElMenu, ElMenuItem, RouterView, ElDivider, TheHeader
  },
  data() {
    return {
      activeIndex: "/",
    }
  }
}
</script>

<template>
  <el-container>
    <el-header height="60px" class="header-container">
      <the-header></the-header>
    </el-header>
    <el-main>
      <router-view></router-view>
    </el-main>
    <el-footer></el-footer>
  </el-container>
</template>

<style scoped>

.header-container {
  border-bottom: solid 1px rgb(228, 231, 237);
}

.logo {
  width: 40px;
  height: 40px;
}

.logo-container {
  text-decoration: none;
  color: inherit;
  display: flex;
  align-items: center;
  gap: 1rem;
  height: 60px;
}

.nav-container {
  height: 60px;
}
</style>
