<template>
    <div class="article-kind">
        <a-card v-for="(item,index) in articleList" :key="index" 
            :title="item.title"> 
            <template #extra>
                <eye-outlined style="color:#aaa"/>
                <span style="color:#aaa">{{item.viewPersonCount}}</span>
                <!-- <a-badge :count="item.viewPersonCount"></a-badge> -->
            </template>
            <p>{{item.content}}</p>
            <a-row class="author-tag">
                <a-col :span="4">{{item.author}}</a-col>           
                <a-col :span="12" class="tags">
                    <span v-for="(tag,k) in item.tags" :key="k">{{tag}}</span>
                </a-col>
                <a-col :span="8">
                    <clock-circle-outlined style="color:#aaa"/>
                    <span style="color:#aaa;margin-left: 5px;">{{item.time}}</span>
                </a-col>
            </a-row>
            

        </a-card>
    </div>
    
</template>
<script>
import {EyeOutlined,ClockCircleOutlined} from '@ant-design/icons-vue';
export default {
    name:"articleKind",
    components:{
        EyeOutlined,
        ClockCircleOutlined
    },
    data(){
        return{
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
    .article-kind{
        padding: 0 40px 20px 80px;
        .author-tag{
            display: flex;
            .tags{
                // margin-left: 30px;
                span{
                    margin-left: 10px;
                    color: rgb(104, 241, 148);
                    border: 1px solid rgb(104, 241, 148);
                    padding: 2px 5px;
                    border-radius: 5px;
                    font-size: 12px;
                }
            }
            
        }
    }
    .ant-card{
        margin-top: 20px;
        box-shadow: -1px 2px 8px #555;
    }
</style>>