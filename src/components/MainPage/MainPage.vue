<script lang="ts">
import MirrorList from './components/MirrorList.vue';
import NewsWidget from './components/NewsWidget.vue';
import { ElContainer, ElCol, ElRow } from 'element-plus/lib/components/index.js';
export default {
    components: {
        MirrorList, ElContainer, ElCol, NewsWidget, ElRow
    }
}
</script>

<template>
    <el-container direction="vertical">
        <el-row class="row-container">
            <el-col :xs="24" :sm="15" :md="13" :lg="11">
                <mirror-list class="container"></mirror-list>
            </el-col>
            <el-col :xs="24" :sm="6" :md="6" :lg="6">
                <news-widget></news-widget>
            </el-col>
        </el-row>
    </el-container>
</template>

<style scoped>
.row-container {
    gap: 40px;
    justify-content: center;
    height: 100%;
}
</style>