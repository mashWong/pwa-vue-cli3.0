<template>
    <div id="app">
        <!--<img src="./assets/logo.png">-->
        <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
        <BackColor />
    </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld.vue'
    import BackColor from './components/backColor.vue'

    export default {
        name: 'app',
        components: {
            HelloWorld,
            BackColor
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        width: 100%;
        height: 100%;
    }
</style>
