<template>
  <el-table :data="projectList" style="width: 100%">
    <el-table-column prop="projectCode" label="项目代码"></el-table-column>
    <el-table-column prop="projectName" label="项目名称"></el-table-column>
    <el-table-column prop="type" label="类型"></el-table-column>
    <el-table-column prop="result" label="结果"></el-table-column>
    <el-table-column label="结果列表">
      <template #default="{ row }">
        <ul v-if="row.resultList">
          <li v-for="(result, index) in row.resultList" :key="index">{{ result }}</li>
        </ul>
        <span v-else>无</span>
      </template>
    </el-table-column>
    <el-table-column prop="normalValue" label="正常值"></el-table-column>
    <el-table-column prop="projectContent" label="项目内容"></el-table-column>
    <el-table-column prop="projectQuota" label="项目配额"></el-table-column>
    <el-table-column prop="complete" label="完成"></el-table-column>
    <el-table-column prop="pass" label="通过" :formatter="passFormatter"></el-table-column>
  </el-table>
</template>

<script>
export default {
  data() {
    return {
      projectList: [
        {
          id: 13644,
          equipmentRelId: 4381,
          inspectionProjectId: 25,
          delFlag: 0,
          projectCode: "SJSX20240000018",
          projectName: "大桃子项目3",
          type: 3,
          result: "洛杉矶湖人帆帆帆帆帆帆帆帆方法发放帆帆帆帆帆帆帆帆方法发放反反复复烦烦烦贩夫贩妇分帆帆帆帆帆帆帆帆方法发fffffffffffff,丹佛掘金反反复复烦烦烦贩夫贩妇分反反复复烦烦烦贩夫贩妇分反反复复烦烦烦贩夫贩妇分反反复复烦烦烦贩夫贩妇分方法方法放法ffffffffffffffffffff,太阳反反复复烦烦烦贩夫贩妇分贩夫贩妇fffff,e帆帆帆帆帆帆帆帆方法发放反反复复烦烦烦贩夫贩妇分方法方法非ffffffff反反复复烦烦烦贩夫贩妇分贩夫贩妇fffffffff",
          resultList: [
            "洛杉矶湖人帆帆帆帆帆帆帆帆方法发放帆帆帆帆帆帆帆帆方法发放反反复复烦烦烦贩夫贩妇分帆帆帆帆帆帆帆帆方法发fffffffffffff",
            "丹佛掘金反反复复烦烦烦贩夫贩妇分反反复复烦烦烦贩夫贩妇分反反复复烦烦烦贩夫贩妇分反反复复烦烦烦贩夫贩妇分方法方法放法ffffffffffffffffffff",
            "太阳反反复复烦烦烦贩夫贩妇分贩夫贩妇fffff",
            "e帆帆帆帆帆帆帆帆方法发放反反复复烦烦烦贩夫贩妇分方法方法非ffffffff反反复复烦烦烦贩夫贩妇分贩夫贩妇fffffffff"
          ],
          normalValue: "1,2,3",
          projectContent: "检查3",
          projectQuota: "日标",
          complete: null,
          pass: false
        },
        {
          id: 13645,
          equipmentRelId: 4381,
          inspectionProjectId: 23,
          delFlag: 0,
          projectCode: "SJSX20240000016",
          projectName: "大桃子项目1",
          type: 1,
          result: "",
          resultList: null,
          normalValue: "",
          projectContent: "检查1",
          projectQuota: "国标",
          complete: null,
          pass: false
        }
        // 其他数据...
      ]
    };
  },
  methods: {
    passFormatter(row, column, cellValue) {
      return cellValue ? '是' : '否';
    }
  }
};
</script>

<style scoped>
/* 可以根据需要添加样式 */
</style>
