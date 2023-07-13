<script lang="ts">
import { ElCard, ElTable, ElTableColumn, ElAutoResizer, ElTag } from 'element-plus/lib/components/index.js';


const data = Array.from({ length: 5 }).map(() => (
    {
        name: "archlinux",
        status: "success",
        size: "100TB",
        lastUpdate: "Today",
        nextUpdate: "Tomorrow",
    }
));

console.log(data);


export default {
    components: {
        ElCard, ElTable, ElAutoResizer, ElTag, ElTableColumn
    },
    data() {
        return {
            tableData: data,
        }
    }
}
</script>


<template>
    <el-card>
        <template #header>
            <div class="card-header">
                <h2>MirrorList</h2>
                <el-button class="button" text>Operation button</el-button>
            </div>
        </template>
        <template>
            <el-table :data="tableData">
                <el-table-column prop="name" label="Name" width="150" />
                <el-table-column prop="status" label="Status" width="150" />
                <el-table-column prop="size" label="size" width="150" />
                <el-table-column prop="lastUpdate" label="lastUpdate" width="150" />
                <el-table-column prop="nextUpdate" label="nextUpdate" width="150" />
            </el-table>
        </template>
    </el-card>
</template>

<style scoped>
.card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.table {
    width: 100%;
    height: 100%;
}
</style>