<template>
    <div class="backpack">
        <div class="headerBar">
            <van-icon class="colse" name="cross" color="#fff" size="0.45rem" @click.native="closeMy" />
        </div>
        <div class="equip">
            <div class="left">
                <div class="current">
                    <div class="currentText">当前使用</div>
                    <div class="name">UMP9 冲锋枪</div>
                    <div class="power">杀伤力: 3</div>
                </div>
                <div>
                    <div class="name">P18C 手枪</div>
                    <div class="power">杀伤力: 3</div>
                </div>
            </div>
            <div class="right">
                <van-row gutter="10" class="arrList">
                    <van-col span="8">
                        <div class="item">
                        </div>
                        <div class="name">1级背包</div>
                    </van-col>
                    <van-col span="8">
                        <div class="item">
                        </div>
                        <div class="name">1级背包</div>
                    </van-col>
                    <van-col span="8">
                        <div class="item">
                        </div>
                        <div class="name">1级背包</div>
                    </van-col>
                    <van-col span="8">
                        <div class="item">
                        </div>
                        <div class="name">1级背包</div>
                    </van-col>
                    <van-col span="8">
                        <div class="item">
                        </div>
                        <div class="name">1级背包</div>
                    </van-col>
                </van-row>
            </div>
        </div>
        <div class="backpackPattern">
            背包（1级）1/10
        </div>
        <van-row class="info">
            <van-col span="8">
                <div class="item">
                    <p class="img"></p>
                    <div>
                        <p>子弹</p>
                        <p>所有枪型均可以使用</p>
                    </div>
                </div>
            </van-col>
            <van-col span="8">
                <div class="item">
                    <p class="img"></p>
                    <div>
                        <p></p>
                        <p></p>
                    </div>
                </div>
            </van-col>
            <van-col span="8">
                <div class="item">
                    <p class="img"></p>
                    <div>
                        <p></p>
                        <p></p>
                    </div>
                </div>
            </van-col>
            <van-col span="8">
                <div class="item">
                    <p class="img"></p>
                    <div>
                        <p></p>
                        <p></p>
                    </div>
                </div>
            </van-col>
            <van-col span="8">
                <div class="item">
                    <p class="img"></p>
                    <div>
                        <p></p>
                        <p></p>
                    </div>
                </div>
            </van-col>
            <van-col span="8">
                <div class="item">
                    <p class="img"></p>
                    <div>
                        <p></p>
                        <p></p>
                    </div>
                </div>
            </van-col>
            <van-col span="8">
                <div class="item">
                    <p class="img"></p>
                    <div>
                        <p></p>
                        <p></p>
                    </div>
                </div>
            </van-col>
            <van-col span="8">
                <div class="item">
                    <p class="img"></p>
                    <div>
                        <p></p>
                        <p></p>
                    </div>
                </div>
            </van-col>
            <van-col span="8">
                <div class="item">
                    <p class="img"></p>
                    <div>
                        <p></p>
                        <p></p>
                    </div>
                </div>
            </van-col>
            <van-col span="8">
                <div class="item">
                    <p class="img"></p>
                    <div>
                        <p></p>
                        <p></p>
                    </div>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁二级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁二级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁二级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁二级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁二级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁二级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁三级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁三级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁三级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁三级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁三级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁三级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁三级背包</p>
                </div>
            </van-col>
            <van-col span="8">
                <div class="lock">
                    <p><i class="iconfont iconsuo"></i></p>
                    <p>解锁三级背包</p>
                </div>
            </van-col>
        </van-row>
    </div>
</template>

<script>
    export default {
        name: "backpack",
        methods:{
            closeMy(){
                this.$emit('closeBackpack')
            }
        }
    }
</script>

<style scoped lang="less">
    .backpack{
        background-color:rgba(0,0,0,0.8);
        width: 350px;
        .headerBar{
            box-sizing: border-box;
            border-bottom: 3px solid #5E6166;
            text-align: right;
            padding: 0.1rem 0.15rem;
        }
        .equip{
            overflow: hidden;
            .left{
                box-sizing: border-box;
                float: left;
                width:50%;
                height: 150px;
                border-right: 1px solid #595C61;
                >div.current{
                    color: #D5AE3F;
                }
                >div:first-child{
                    border-bottom: 1px solid #595C61;
                }
                >div{
                    height: 50%;
                    box-sizing: border-box;
                    background-repeat: no-repeat;
                    background-position: center center;
                    background-size:auto 70%;
                    position: relative;
                    color: #fff;
                    font-weight: bold;
                    font-size: 0.24rem;
                    .name{
                        position: absolute;
                        right: 5px;
                        top: 2px;
                    }
                    .currentText{
                        position: absolute;
                        left: 5px;
                        top: 2px;
                    }
                    .power{
                        position: absolute;
                        right: 5px;
                        bottom: 2px;
                        padding: 2px 5px;
                        background-color: #17191D;
                        border: 1px solid #505357;
                        color: #fff;
                    }
                }
                >div{
                    background-image: url("../../assets/images/test-P18C.png");
                }
                >div:first-child{
                    background-image: url("../../assets/images/test-UMP9.png");
                }
            }
            .right{
                float: left;
                width: 50%;
                box-sizing: border-box;
                padding:5px;
                .item{
                    border: 1px solid #938140;
                    height: 45px;
                    background-color:rgba(255,255,255,0.22);
                    background-position: center center;
                    -webkit-background-size: 80%;
                    background-size: 80%;
                    background-repeat: no-repeat;
                }
                .item:first-child{
                    background-image: url("../../assets/images/test-1jibao.png");
                }
                .name{
                    border: 1px solid #56595E;
                    background-color: #17191D;
                    color: #fff;
                    font-size: 0.2rem;
                    margin-top: 1px;
                    margin-bottom: 5px;
                    text-align: center;
                }
            }
        }
        .info{
            overflow: hidden;
            box-sizing: border-box;
            color: #fff;
            height: 350px;
            overflow-y: auto;
            >div:first-child .item .img{
                background-image: url("../../assets/images/test-zidan.png");
            }
            >div{
                border: 1px solid #220703;
                background-color: rgba(255, 255, 255, 0.49);
                height: 57px;
                overflow: hidden;
                .lock{
                    text-align: center;
                    p:first-child{
                        margin-top: 10px;
                        margin-bottom: 8px;
                    }
                }
                .item{
                    overflow: hidden;
                    .img{
                        float: left;
                        width: 50%;
                        height: 55px;
                        background-repeat: no-repeat;
                        background-position: center center;
                        -webkit-background-size: 80%;
                        background-size: 80%;
                        background-color: rgba(255, 255, 255, 0.49);
                    }
                    >div{
                        float: left;
                        width: 50%;
                        font-size: 0.20rem;
                        box-sizing: border-box;
                        padding: 5px 0;
                        padding-left: 3px;
                        p:first-child{
                            margin-bottom: 1px;
                        }
                    }
                }
            }
        }
        .backpackPattern{
            font-size: 16px;
            line-height: 40px;
            color: #fff;
            background-color: rgba(213,174,63,0.8);
            text-align: center;
            font-weight: bold;
            text-shadow:1px 1px 2px #000;
        }
    }
</style>