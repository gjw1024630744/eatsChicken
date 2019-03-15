<template>
    <div class="headers">
        <div class="userImage">
            <div class="imgBox"
                 style="background-image: url('http://img2.imgtn.bdimg.com/it/u=3633606202,875705726&fm=26&gp=0.jpg')"></div>
        </div>
        <div class="centerInfo">
            <p>玩家昵称: 李堃</p>
            <p>战队名称: 最强战队</p>
            <p>枪号: <span>25</span> 枪型: <span>机枪</span></p>
            <p>血量
                <progress-bar :allNum="'16'" :currentNum="'10'" :bgColor="'#ccc'" :borderColor="'#fff'"></progress-bar>
                16
            </p>
            <p>护具
                <progress-bar :allNum="'3'" :currentNum="'1'" :bgColor="'#ccc'" :borderColor="'#fff'"></progress-bar>
                3
            </p>
        </div>
        <div class="rightInfo">
            <p>游戏状态 准备</p>
            <p>游戏时间 12:00</p>
            <p>剩余人数 20</p>
            <div class="poisonRing"><i class="iconfont icondupinweixian"></i>毒圈刷新: 03:00</div>
        </div>
    </div>
</template>

<script>
    import progressBar from '@/components/home/Progressbar'

    export default {
        name: "headers",
        components: {
            progressBar
        },
    }
</script>

<style scoped lang="less">
    .userImage {
        float: left;
        width: 30%;

        .imgBox {
            width: 1.7rem;
            height: 1.7rem;
            margin: 0 auto;
            background-repeat: no-repeat;
            -webkit-background-size: 100%;
            background-size: 100%;
            background-position: center center;
            margin-top: 0.2rem;
        }
    }

    .centerInfo {
        float: left;
        width: 35%;

        p {
            font-size: 0.26rem;
            line-height: 0.45rem;

            span {
                background: #000;
                padding: 0.05rem 0.1rem;
            }
        }
    }

    .rightInfo {
        float: left;
        width: 35%;

        p {
            background-color: #000;
            padding: 0.07rem 0.2rem;
            margin: 0.1rem auto;
            width: 1.7rem;
        }

        .poisonRing {
            i {
                font-size: 0.4rem;
                background-color: #fcfb00;
                color: #000;
                border-radius: 50%;
                margin-right: 0.1rem;
                margin-left: 0.15rem;
            }
        }
    }
</style>