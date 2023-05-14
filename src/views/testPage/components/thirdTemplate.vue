<template>
    <div class="mt10">
        <div class="top">
            <div class="line"></div>
            <div class="title">
                <i class="el-icon-warning"></i>
                补充协议
            </div>
            <div class="line"></div>
        </div>
        <div class="content">
            <el-tabs type="border-card">
  <el-tab-pane label="补充协议1">
    协议内容1：
    <div class="pd10"></div>
</el-tab-pane>
  <el-tab-pane label="补充协议2">
    协议内容2：
    <div class="pd10"></div>
</el-tab-pane>
  <el-tab-pane label="补充协议3">
    协议内容3：
    <div class="pd10"></div>
</el-tab-pane>
</el-tabs>
        </div>
    </div>
</template>

<style lang="scss">
.mt10{
    margin-top: 10px;
}
.top{
    display: flex;
    justify-content: center;
    align-items: center;
    .line{
        width: 47%;
        height: 2px;
        background: #DBDBDB;
        // background-color: #f5f7fa
    }
    .title{
        padding: 0 4px;
    }
}
.pd10{
    padding: 100px;
    background-color: #f8f8f8;
}
</style>