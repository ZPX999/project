<template>
  <div>
    <el-table
    :data="tableData"
    border
    style="width: 90%">
    
        <el-table-column
        prop="Name"
        label="姓名"
        width="120">
        </el-table-column>
        <el-table-column
        prop="kind"
        label="社团类型"
        width="120">
        </el-table-column>
        <el-table-column
        prop="ccName"
        label="社团名称"
        width="120">
        </el-table-column>
        <el-table-column
        prop="Phone"
        label="电话"
        width="120">
        </el-table-column>
        <el-table-column
        prop="Email"
        label="邮箱"
        width="120">
        </el-table-column>
        <el-table-column
        prop="Number"
        label="数字"
        width="120">
        </el-table-column>
        <el-table-column
        prop="web"
        label="网址"
        width="120">
        </el-table-column>
        <el-table-column
        prop="Message"
        label="信息"
        width="120">
        </el-table-column>
        <el-table-column
        fixed="right"
        label="操作"
        width="100">
        <template slot-scope="scope">
            <el-button @click="handle(scope.row)" type="text" size="small">审核</el-button>
            <el-button @click="deleteinfo(scope.$index,tableData)" type="text" size="small">删除</el-button>
        </template>
        </el-table-column>
        
    </el-table>
  </div>
</template>

<script>
export default {
    name:'RequestList',
    data() {
        return {
            tableData: [
                {
                    Name:'张三',
                    kind:"11",
                    coName:"11",
                    Number:12,
                    QQ:"123",
                    Phone:"111",
                    web:"www.",
                    Message:"666",
                    Email:"@...",
                },
                {
                    Name:'张三',
                    kind:"11",
                    coName:"11",
                    Number:12,
                    QQ:"123",
                    Phone:"111",
                    web:"www.",
                    Message:"666",
                    Email:"@...",
                },
                {
                    Name:'张三',
                    kind:"11",
                    coName:"11",
                    Number:12,
                    QQ:"123",
                    Phone:"111",
                    web:"www.",
                    Message:"666",
                    Email:"@...",
                },
            ],
        }
    },
    methods: {
        handle(row) {
            console.log(row);
        },
        deleteinfo(index,row) {
            row.splice(index,1);
        }
    },
}
</script>

<style>
@import url("//unpkg.com/element-ui@2.15.13/lib/theme-chalk/index.css");
</style>