<template>
    <div class="home">
        <baidu-map
                :center="center"
                :zoom="zoom"
                @ready="handler"
                map-type="BMAP_HYBRID_MAP"
                class="map-view">
        </baidu-map>
    </div>
</template>

<script>
    export default {
        name: 'home',
        components: {},
        data() {
            return {
                center: {lng: 0, lat: 0},
                zoom: 0,
                BMap:null,
                map:null
            }
        },
        methods: {
            handler({BMap, map}) {
                this.BMap = BMap
                this.map = map
                let _this = this
                // console.log(BMap, map)
                this.zoom = 19
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
            }
        }
    }
</script>

<style scoped lang="less">
    .map-view {
        position: fixed;
        left: 0;
        top: 0;
        right: 0;
        bottom: 0;
    }
</style>
