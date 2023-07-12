<script lang="ts">
import { ElContainer, ElHeader, ElFooter, ElMain, ElRow, ElCol, ElMenu, ElMenuItem, ElDivider } from 'element-plus/lib/components/index.js';
import { RouterView, RouterLink } from 'vue-router';
export default {
  components: {
    ElContainer, ElHeader, ElFooter, ElMain, ElRow, ElCol, ElMenu, ElMenuItem, RouterView, RouterLink, ElDivider
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
    <el-header align="center" class="header">
      <el-row :gutter="20">
        <el-col :span="8" align="center">
          <router-link to="/" class="logo-container">
            <img class="logo" src="./assets/osa.png" alt="" />
            <div>
              <h1>HITsz OSA Mirror</h1>
            </div>
          </router-link>
        </el-col>
        <el-col :span="8"></el-col>
        <el-col :span="8" align="center">
          <nav class="nav-container">
            <el-menu mode="horizontal" :default-active="activeIndex" :router="true">
              <el-menu-item index="/">
                Home
              </el-menu-item>
              <el-menu-item index="/news">
                News
              </el-menu-item>
            </el-menu>
          </nav>
        </el-col>
      </el-row>
    </el-header>
    <el-main>
      <router-view></router-view>
    </el-main>
    <el-footer></el-footer>
  </el-container>
</template>

<style scoped>
.header {
  border-bottom: solid 1px var(--el-menu-border-color);
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
