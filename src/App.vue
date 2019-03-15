<template>
    <div id="app">
        <!--<div id="nav">-->
            <!--<router-link to="/">Home</router-link>-->
            <!--|-->
            <!--<router-link to="/about">About</router-link>-->
        <!--</div>-->
        <router-view/>
    </div>
</template>

<style lang="less">
    body {
        font-size: 0.24rem;
    }
    html,body{
        width: 100%;
        height: 100%;
    }
    #app {
        width: 100%;
        height: 100%;
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
    }
    *{
        padding:0;
        margin: 0;
    }
</style>
