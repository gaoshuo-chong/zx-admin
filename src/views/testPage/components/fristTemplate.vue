<template>
    <div>
        <div class="top">
            <div class="line"></div>
            <div class="title">
                <i class="el-icon-warning"></i>
                协议主体
            </div>
            <div class="line"></div>
        </div>
        <div class="content">
            <el-form :inline="true" :model="formInline" class="demo-form-inline">
  <el-form-item label="协议客户：" style="width:50%">
    <el-button size="small">选择客户</el-button>
    <span>上海正也科技有限公司</span>
  </el-form-item>
  <el-form-item label="协议状态：">
    <el-select v-model="formInline.region" placeholder="协议状态：">
      <el-option label="正常" value="0"></el-option>
      <el-option label="不正常" value="1"></el-option>
    </el-select>
  </el-form-item>
</el-form>
<el-form :inline="true" :model="formInline" class="demo-form-inline">
  <el-form-item label="购进指标："  style="width:50%">
    <el-form :inline="true" :model="formInline" class="demo-form-inline">
    <el-form-item label="">
        <el-select v-model="formInline.money" placeholder="" size="small" style="width:80px;">
            <el-option label="金额" value="0"></el-option>
            <el-option label="不金额" value="1"></el-option>
        </el-select>
    </el-form-item>
    <el-form-item label="">
        <el-input v-model="formInline.num" placeholder="输入金额/数量" class="testinput" disabled></el-input>
    </el-form-item>
    </el-form>
    </el-form-item>
  <el-form-item label="纯销指标：">
    <el-form :inline="true" :model="formInline" class="demo-form-inline">
    <el-form-item label="">
        <el-select v-model="formInline.money" placeholder="" size="small" style="width:80px;">
            <el-option label="金额" value="0"></el-option>
            <el-option label="不金额" value="1"></el-option>
        </el-select>
    </el-form-item>
    <el-form-item label="">
        <el-input v-model="formInline.num" placeholder="输入金额/数量" class="testinput" disabled></el-input>
    </el-form-item>
    </el-form>
  </el-form-item>
</el-form>

<el-form :inline="true" :model="formInline" class="demo-form-inline">
  <el-form-item label="销售区域：" style="width:50%">
    <el-select v-model="formInline.region" placeholder="选择区域：">
      <el-option label="区域" value="0"></el-option>
      <el-option label="不区域" value="1"></el-option>
    </el-select>
  </el-form-item>
  <el-form-item label="签订时间：">
    <el-date-picker
    style="width:390px"
      v-model="timeValue"
      type="datetime"
      placeholder="选择日期时间"
      default-time="12:00:00">
    </el-date-picker>
  </el-form-item>
</el-form>

<el-form :inline="true" :model="formInline" class="demo-form-inline">
    <el-form-item label="购进渠道：">
        <el-select v-model="formInline.region" placeholder="指定渠道">
      <el-option label="指定渠道" value="0"></el-option>
      <el-option label="不指定渠道" value="1"></el-option>
    </el-select>
    <el-button size="small" style="margin-left: 10px;">请选择渠道</el-button>
  </el-form-item>
</el-form>

<div style="padding:0 70px">
<el-table
      :data="tableData"
      style="width: 100%">
      <el-table-column
        prop="date"
        label="指定渠道编码"
        >
      </el-table-column>
      <el-table-column
        prop="name"
        label="指定渠道名称"
        >
      </el-table-column>
      <el-table-column
        prop="address"
        label="所在省">
      </el-table-column>
    </el-table>
</div>
        </div>
    </div>
</template>

<script>
 export default {
    data() {
      return {
        formInline: {
          user: '',
          region: '0',
          money:'0',
          num:''
        },
        timeValue:'',
        tableData: [{
            date: '100010',
            name: '宁波九州通药业有限公司',
            address: '浙江省'
          }, {
            date: '10011',
            name: '宁波八州通药业有限公司',
            address: '安徽省'
          }, {
            date: '10012',
            name: '宁波七州通药业有限公司',
            address: '浙江省'
          }]
      }
    },
    methods: {
      onSubmit() {
        console.log('submit!');
      }
    }
  }
</script>

<style lang="scss">
.top{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;
    .line{
        width: 47%;
        height: 2px;
        background: #DBDBDB;
        // background-color: #C0C4CC;
        // background:  rgb(48, 65, 86);
    }
    .title{
        padding: 0 4px;
    }
}
.content{
    padding: 12px 16px;
    background: #fff;
    el-form-item{
        width: 47%!important;
    }
}
.el-step__icon.is-text{
    display: none !important;
}
.testinput{
    padding-left: 10px;
    width: 300px;
}
</style>