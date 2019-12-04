<template>
  <div class="main">
    <el-table :data="tableData" border height="600px" style="width: 100%">
      <el-table-column fixed label="日期" prop="date" width="150"></el-table-column>
      <el-table-column label="姓名" prop="name" width="120"></el-table-column>
      <el-table-column label="省份" prop="province" width="120"></el-table-column>
      <el-table-column label="市区" prop="city" width="120"></el-table-column>
      <el-table-column label="地址" prop="address"></el-table-column>
      <el-table-column label="邮编" prop="zip" width="120"></el-table-column>
      <el-table-column fixed="right" label="操作" width="100">
        <template slot-scope="scope">
          <el-button @click="handleClick(scope.row)" size="small" type="text">查看</el-button>
          <el-button size="small" type="text">编辑</el-button>
        </template>
      </el-table-column>
    </el-table>
    <el-pagination :total="1000" background class="text-center" layout="total, prev, pager, next" style="padding:20px;"></el-pagination>
  </div>
</template>

<script>
export default {
  methods: {
    handleClick(row) {
      console.log(row);
    }
  },

  data() {
    return {
      tableData: Array(20).fill({
        date: "2016-05-02",
        name: "王小虎",
        province: "上海",
        city: "普陀区",
        address: "上海市普陀区金沙江路 1518 弄",
        zip: 200333
      })
    };
  }
};
</script>