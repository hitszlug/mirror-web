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
            <el-col :xs="24" :sm="13" :md="13" :lg="11">
                <mirror-list class="container"></mirror-list>
            </el-col>
            <el-col :xs="24" :sm="9" :md="9" :lg="6" class="right-col">
                <news-widget></news-widget>
                <news-widget></news-widget>
            </el-col>
        </el-row>
    </el-container>
</template>

<style scoped>
.row-container {
    gap: 20px;
    justify-content: center;
    height: 100%;
}

.right-col {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

@media screen and (min-width: 992px) {
    .row-container {
        gap: 40px;
    }
}
</style>