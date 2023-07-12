<script lang="ts">
import { ElCard, ElTableV2 } from 'element-plus/lib/components/index.js';

export default {
    components: {
        ElCard, ElTableV2
    }
}
</script>


<template>
    <el-card class="box-card">
        <template #header>
            <div class="card-header">
                <h2>MirrorList</h2>
                <el-button class="button" text>Operation button</el-button>
            </div>
        </template>
        <div>
            <!-- <el-table-v2 :columns="columns" :data="data" :width="700" :height="400" fixed /> -->
        </div>
    </el-card>
</template>

<style scoped>
.card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.text {
    font-size: 14px;
}

.item {
    margin-bottom: 18px;
}

.box-card {
    width: 100%;
}
</style>