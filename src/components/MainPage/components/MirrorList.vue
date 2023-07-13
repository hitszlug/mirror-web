<script lang="ts">
import { ElCard, ElTableV2, ElAutoResizer, Column, ElTag } from 'element-plus/lib/components/index.js';
import { h } from 'vue';
// const columns = generateColumns();
// const data = generateData(columns, 20);

let id = 0;
const dataGenerator = () => (
    {
        id: `archlinux-${id++}`,
        name: "archlinux",
        status: "success",
        size: "100TB",
        lastUpdate: "Today",
        nextUpdate: "Tomorrow",
    }
)

const columns: Column<any>[] = [
    {
        key: 'name',
        title: 'Name',
        dataKey: 'name',
        width: 120,
    },
    {
        key: 'status',
        title: 'Status',
        dataKey: 'status',
        width: 100,
        cellRenderer: ({ cellData: status }) => h(
            ElTag,
            { type: status, "disable-transitions": true },
            status
        )
    },
    {
        key: 'size',
        title: 'Size',
        dataKey: 'size',
        width: 120,
    },
    {
        key: 'lastUpdate',
        title: 'Last Update',
        dataKey: 'lastUpdate',
        width: 150,
    },
    {
        key: 'nextUpdate',
        title: 'Next Update',
        dataKey: 'nextUpdate',
        width: 150,
    },

]

export default {
    components: {
        ElCard, ElTableV2, ElAutoResizer, ElTag
    },
    data() {
        return {
            columns,
            data: Array.from({ length: 40 }).map(dataGenerator)
        }
    }
}
</script>


<template>
    <el-tag style="display: none;"></el-tag>
    <el-card class="box-card">
        <template #header>
            <div class="card-header">
                <h2>MirrorList</h2>
                <el-button class="button" text>Operation button</el-button>
            </div>
        </template>
        <div class="table-container">
            <el-auto-resizer>
                <template #default="{ height, width }">
                    <el-table-v2 :columns="columns" :data="data" :height="height" :width="width" fixed />
                </template>
            </el-auto-resizer>
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

.table-container {
    height:900px;
    width: 100%;
}
</style>