<template>
    <div class="mt10">
        <div class="top">
            <div class="line"></div>
            <div class="title">
                <i class="el-icon-warning"></i>
                产品政策
            </div>
            <div class="line"></div>
        </div>
        <div class="message">
            <el-button type="primary">添加产品</el-button>
            <div class="flx">
                <div>购进总指标（万元）：￥152.65</div>
                <div>指标按季度分解（万元）：【Q1】￥12.5,【Q1】￥12.5,【Q1】￥12.5,【Q1】￥12.5</div>
                <div>纯销总指标（万元）：￥152.65</div>
            </div>
        </div>
        <div class="content">
            <el-card class="box-card">
  <div slot="header" class="clearfix">
    <span class="titleText">产品：</span>
    <el-button size="mini">选择产品</el-button>
    <span class="titleText ml40">头孢胶丸 24粒/盒</span>
    <span class="titleText ml139">协议效期：        2020-02-01 - 2020-05-01</span>
    <el-button style="float: right; padding: 7px 9px;color: yellowgreen;" >删除</el-button>
  </div>
  <!-- <div v-for="o in 4" :key="o" class="text item">
    {{'列表内容 ' + o }}
  </div> -->
  <el-table
      :data="tableData"
      style="width: 100%">
      <el-table-column
        prop="date"
        label="协议价（元）"
        >
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="name"
        label="票折（元）"
        >
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="购进指标量（大单位）">
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="购进指标量（小单位）">
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="购进金额（万元）">
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="纯销指标量（小单位）">
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="纯销指标金额（万元）">
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
    </el-table>

    <el-table
      :data="tableDatas"
      style="width: 100%">
      <el-table-column
        prop="date"
        label="分销奖励"
        >
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="name"
        label="费用科目"
        >
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="零售配送">
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="费用科目">
        <template slot-scope="scope">
            <el-select v-model="formInline.money" placeholder="单选项" size="small">
            <el-option label="金额" value="0"></el-option>
            <el-option label="不金额" value="1"></el-option>
        </el-select>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="医疗配送商">
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="费用科目">
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="自定义7">
        <template slot-scope="scope">
            <el-date-picker
      v-model="timeValue"
      type="datetime"
      placeholder="选择日期时间"
      default-time="12:00:00">
    </el-date-picker>
      </template>
      </el-table-column>
      <el-table-column
        prop="address"
        label="自定义8">
        <template slot-scope="scope">
            <el-input v-model="formInline.num" placeholder="请输入"></el-input>
      </template>
      </el-table-column>
    </el-table>
</el-card>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            tableData: [

            {
            date: '100010',
            name: '宁波九州通药业有限公司',
            address: '浙江省'
          }
            ],
            tableDatas: [
            {
            date: '100010',
            name: '宁波九州通药业有限公司',
            address: '浙江省'
          }
            ],
            formInline:{
                num:'',
                money:''
            },
            timeValue:''
        }
    }
}
</script>

<style lang="scss">
.mt30{
    margin-top: 10px;
}
.ml40{
    margin-left: 40px;
    color:  #1890ff;
}
.ml139{
    margin-left: 139px;
}
.flx{
    width: 100%;
    display: flex;
    font-size: 12px;
    justify-content: space-around;
}
.top{
    display: flex;
    justify-content: center;
    align-items: center;
    .line{
        width: 47%;
        height: 2px;
        background: #DBDBDB;
        // background-color: #C0C4CC;
    }
    .title{
        padding: 0 4px;
    }
}
.message{
    width: 70%;
    display: flex;
    align-items: center;
}

.text {
    font-size: 14px;
  }

  .item {
    margin-bottom: 18px;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }

  .box-card {
    width: 100%;
  }
  .titleText{
    display: inline-block!important;
    font-size: 12px;
  }
</style>