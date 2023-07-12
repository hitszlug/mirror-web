<script lang="ts">
import { ElCard } from 'element-plus/lib/components/index.js';
export default {
    components: {
        ElCard
    }
}
</script>


<template>
    <el-card class="box-card">
        <template #header>
            <div class="card-header">
                <h2>What's New</h2>
            </div>
        </template>
        <div v-for="o in 4" :key="o" class="text item">{{ 'List item ' + o }}</div>
    </el-card>
</template>

<style scoped>
.card-header {
    display: flex;
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