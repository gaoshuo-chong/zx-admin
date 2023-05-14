<template>
    <div class="content">
        <fristTemplate></fristTemplate>
        <secondTemplate></secondTemplate>
        <thirdTemplate></thirdTemplate>
        <el-button type="primary">保存</el-button>
    </div>
</template>

<script>
import fristTemplate from './components/fristTemplate'
import secondTemplate from './components/secondTemplate'
import thirdTemplate from './components/thirdTemplate'
export default{
    components:{
        fristTemplate,
        secondTemplate,
        thirdTemplate
    },
    data(){
        return{

        }
    }
}
</script>

<style lang="scss" scoped>
.content{
    height: 100%;
    padding: 20px;
    // background: #f8f8f8;
    background: #F7F7F7;
}
</style>