<template>
    <a-layout>
        <a-layout-header>
            <a-row>
                <a-col :lg="2" :sm="3">学习之路</a-col>
                <a-col :lg="1"></a-col>
                <a-col :lg="8" :sm="13" >
                    <div class="index-tab">
                        <div>首页</div>
                        <div>文章分类</div>
                        <div>标签</div>
                        <div>文章归档</div>
                        <div>写文章</div>
                    </div> 
                </a-col>
                <a-col :lg="2"></a-col>
                <a-col :lg="4" :sm="4">
                    <a-input placeholder="请输入搜索内容"></a-input>
                </a-col>
                <a-col :lg="1"></a-col>
                <a-col :lg="4" :sm="4" class="index-action">
                    <div>登录</div>
                    <div>注册</div>
                </a-col>
            </a-row>
        </a-layout-header>
        <a-layout>
        <a-layout-content>
            <article-kind></article-kind>
        </a-layout-content>
        <a-layout-sider>
            <sider></sider>
        </a-layout-sider>
        </a-layout>
        <!-- <a-layout-footer>Footer</a-layout-footer> -->
    </a-layout>
    
    
</template>
<script>
import articleKind from './articleKind.vue'; 
import sider from "./sider.vue";
export default {
    name:"Index",
    components:{
        articleKind,
        sider
    }

}
</script>
<style lang="less" scoped>
    .index-tab{
        display: flex;
        justify-content: space-around;
    }
    .index-action{
        display: flex;
        justify-content: space-around;
    }
    :deep(.ant-layout-header) {
        background-color: #fff !important;
    }
    :deep(.ant-layout-sider) {
        margin-top: 20px;
        background-color: #f0f2f5 !important;
        padding-right: 40px;
        width: 35% !important;
        flex: 0 0 35% !important;
        max-width: 35% !important;
        min-width: 35% !important;
    }

</style>
