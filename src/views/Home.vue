<template>
    <div class="home">
        <baidu-map
                :center="center"
                :zoom="zoom"
                @ready="handler"
                map-type="BMAP_HYBRID_MAP"
                class="map-view">
            <bm-scale></bm-scale>
        </baidu-map>
        <div class="content">
            <page-header></page-header>
            <div class="selectBar">
                <div class="btnItem Combat-Team">战 队</div>
                <div class="btnItem notice">通 知</div>
            </div>
            <div class="operations">
                <div class="item">
                    <img src="@/assets/images/up-charger.png" alt="">
                    <p>上弹夹</p>
                    <span class="tips">01</span>
                </div>
                <div class="item">
                    <img src="@/assets/images/drug.png" alt="">
                    <p>补血</p>
                    <span class="tips">02</span>
                </div>
                <div class="item" @click="changeGun">
                    <img src="@/assets/images/gun.png" alt="">
                    <p>换枪</p>
                    <span class="tips">03</span>
                </div>
                <div class="item" @click="backpackState = true">
                    <img src="@/assets/images/package.png" alt="">
                    <p>背包</p>
                    <span class="tips">01</span>
                </div>
            </div>
        </div>
        <van-popup v-model="backpackState" :overlay="false" class="pageBackpack">
            <page-backpack @closeBackpack="backpackState = false"></page-backpack>
        </van-popup>
    </div>
</template>

<script>
    import { Toast } from 'vant';
    import pageHeader from '@/components/home/header'
    import pageBackpack from '@/components/home/backpack'
    export default {
        name: 'home',
        components: {
            pageHeader,pageBackpack
        },
        data() {
            return {
                center: {lng: 0, lat: 0},
                zoom: 0,
                BMap:null,
                map:null,
                backpackState:false
            }
        },
        methods: {
            // 地图加载完成回调
            handler({BMap, map}) {
                this.BMap = BMap
                this.map = map
                let _this = this
                // console.log(BMap, map)
                this.zoom = 18
                let geolocation = new this.BMap.Geolocation();
                geolocation.getCurrentPosition( r => {
                    if(r.point){
                        _this.center.lng = r.point.lng
                        _this.center.lat = r.point.lat
                        console.log('定位成功')
                    }else{
                        console.log('定位失败')
                    }
                })
            },
            // 换枪
            changeGun(){
                //......请求操作
                Toast.loading({
                    mask: false,
                    message: '换枪中...'
                });
                // this.$notify('提示文案');
            }
        }
    }
</script>

<style scoped lang="less">
    .map-view,.home{
        width: 100%;
        height: 100%;
    }
    .content {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        /*border: 1px solid #f00;*/
        background: url("../assets/images/header_bg.png") no-repeat top center;
        background-size: 100%;
        overflow: hidden;
        color: #fff;
        padding: 10px 0;
    }
    .selectBar{
        clear: both;
        overflow: hidden;
        .btnItem{
            float: left;
            height: 0.8rem;
            line-height: 0.9rem;
            background-color:rgba(0,0,0,0.6);
            color: #cfaa43;
            font-size: 0.3rem;
            font-weight: bold;
            margin-right: 0.1rem;
            background-position: 0.2rem center;
            background-repeat: no-repeat;
            -webkit-background-size: 0.5rem;
            background-size: 0.55rem;
            padding-left: 0.8rem;
            padding-right: 0.2rem;
        }
        .Combat-Team{
            background-image: url("../assets/images/Combat-team-icon.png");
        }
        .notice{
            background-image: url("../assets/images/notice-icon.png");
            background-size: 0.48rem;
        }
    }
    .operations{
        position: fixed;
        left: 0;
        top: 3.8rem;
        width: 1.4rem;
        .item{
            img{
                width: 70%;
                margin: 0 auto;
            }
            p{
                padding-bottom: 0.1rem;
            }
            .tips{
                position: absolute;
                right: -0.2rem;
                top: -0.1rem;
                color: #000;
                background-color: #F1C444;
                font-size: 0.24rem;
                font-weight: bold;
                font-family: "Microsoft YaHei UI";
                width: 0.5rem;
                height: 0.4rem;
                line-height: 0.4rem;
                border-radius: 0.2rem;
            }
            text-align: center;
            background-color:rgba(0,0,0,0.6);
            margin-top: 0.1rem;
            position: relative;
        }
    }
    .pageBackpack{
        background: none;
    }
</style>
