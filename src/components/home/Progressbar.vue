<template>
    <div class="Progressbar" :style="{'border':'1px solid '+borderColor}">
        <div class="num" :style="{'transition':'0.3s','backgroundColor':bgColor,'width':unmWidth+'%'}"></div>
    </div>
</template>

<script>
    export default {
        name: "Progressbar",
        props: {
            allNum: {  // 必须提供字段
                required: true
            },
            currentNum: {  // 必须提供字段
                required: true
            },
            bgColor: {   // 可选字段，有默认值
                default: '#000'
            },
            borderColor: {   // 可选字段，有默认值
                default: '#000'
            }
        },
        data(){
            return{
                unmWidth:10
            }
        },
        watch:{
            currentNum(val){
                this.unmWidth = val/this.allNum*100;
            }
        },
        mounted(){
            this.unmWidth = this.currentNum/this.allNum*100;
        }
    }
</script>

<style scoped lang="less">
    .Progressbar{
        display: inline-block;
        width: 1.6rem;
        height: 0.2rem;
        position: relative;
        top: 0.02rem;
        .num{
            height: 100%;
            float: left;
        }
    }
</style>