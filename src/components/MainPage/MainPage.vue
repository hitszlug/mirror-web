<script lang="ts">
import MirrorList from './components/MirrorList.vue';
import NewsWidget from './components/NewsWidget.vue';
import { ElContainer, ElCol } from 'element-plus/lib/components/index.js';
export default {
    components: {
        MirrorList, ElContainer, ElCol,NewsWidget
    }
}
</script>

<template>
    <el-container>
        <el-col :xs="0" :sm="1" :md="2" :lg="3"></el-col>
        <el-col :xs="24" :sm="15" :md="13" :lg="11">
            <mirror-list class="mirror-list"></mirror-list>
        </el-col>
        <el-col :xs="0" :sm="1" :md="1" ></el-col>
        <el-col :xs="0" :sm="6" :md="6" :lg="6">
            <news-widget class="mirror-list"></news-widget>
        </el-col>
        <el-col :xs="0" :sm="1" :md="2" :lg="3"></el-col>
    </el-container>
</template>

<style scoped></style>