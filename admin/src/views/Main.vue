<template>
  <div>
    <el-container style="height: 100vh;">
      <el-aside width="200px" style="background-color: rgb(238, 241, 246)">
        <el-menu router :default-openeds="['1', '3']">
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-message"></i>内容管理
            </template>
            <el-menu-item-group>
              <template slot="title">分类</template>
              <el-menu-item index="/categories/create">新建分类</el-menu-item>
              <el-menu-item index="/categories/list">分类列表</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
        </el-menu>
      </el-aside>

      <el-container>
        

        <el-main>
            <router-view></router-view>
          <!-- <el-table :data="tableData">
            <el-table-column prop="date" label="日期" width="140"></el-table-column>
            <el-table-column prop="name" label="姓名" width="120"></el-table-column>
            <el-table-column prop="address" label="地址"></el-table-column>
          </el-table> -->
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>



<style>
.el-header {
  background-color: #b3c0d1;
  color: #333;
  line-height: 60px;
}

.el-aside {
  color: #333;
}
</style>

<script>
export default {
  data() {//这个地方是怎么删除的
    const item = {
      date: "2016-05-02",
      name: "王小虎",
      address: "上海市普陀区金沙江路 1518 弄"
    };
    return {
      tableData: Array(20).fill(item)
    };
  }
};
</script>