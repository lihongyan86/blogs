<template>
    <div class="sider">
        <a-card  title="最热标签" > 
            <template #extra>
                <!-- <eye-outlined style="color:#aaa"/> -->
                <a>查看更多</a>
                <!-- <a-badge :count="item.viewPersonCount"></a-badge> -->
            </template>
            <div class="tags">
                <div v-for="(item,index) in tags" :key="index">{{item}}</div>
            </div>
            
            <!-- <p>{{item.content}}</p> -->
            <!-- <a-row class="author-tag">
                <a-col :span="4">{{item.author}}</a-col>           
                <a-col :span="12" class="tags">
                    <span v-for="(tag,k) in item.tags" :key="k">{{tag}}</span>
                </a-col>
                <a-col :span="8">
                    <clock-circle-outlined style="color:#aaa"/>
                    <span style="color:#aaa;margin-left: 5px;">{{item.time}}</span>
                </a-col>
            </a-row> -->
            

        </a-card>
    </div>
    
</template>
<script>
import {EyeOutlined,ClockCircleOutlined} from '@ant-design/icons-vue';
export default {
    name:"sider",
    components:{
        EyeOutlined,
        ClockCircleOutlined
    },
    data(){
        return{
            tags:["vue","springboot","node.js","typescript"],
            articleList:[
            {
                title:"文章1",
                description:"111",
                content:"11111",
                author:"李一",
                tags:["前端","vue"],
                viewPersonCount:"23",
                time:"2022-09-27 09:56:43"
            },
            {
                title:"文章2",
                description:"222",
                content:"2222",
                author:"李二",
                tags:["前端"],
                viewPersonCount:"23",
                time:"刚刚"
            },
            {
                title:"文章1",
                description:"111",
                content:"11111",
                author:"李一",
                tags:["前端","react"],
                viewPersonCount:"23",
                time:"2022-09-27 09:56:43"
            },
            {
                title:"文章1",
                description:"111",
                content:"11111",
                author:"李一",
                tags:["前端","angular"],
                viewPersonCount:"23",
                time:"2022-09-27 09:56:43"
            },
            {
                title:"文章1",
                description:"111",
                content:"11111",
                author:"李一",
                tags:["前端","js"],
                viewPersonCount:"23",
                time:"2022-09-27 09:56:43"
            },
        ]
        }
        
    }
}
</script>
<style lang="less" scoped>
    .ant-card {
        background-color: #fff;
    }
    .tags{
        display: flex;
        flex-wrap: wrap;
        div{
            margin-right: 10px;
            color: rgb(104, 241, 148);
            border: 1px solid rgb(104, 241, 148);
            padding: 2px 5px;
            border-radius: 5px;
            font-size: 12px;
            margin-bottom: 10px;
        }
    }
</style>>