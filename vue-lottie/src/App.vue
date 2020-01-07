<template>
    <div id="app">
        <div class="animation-style" ref="animation"></div>
        <HelloWorld msg="Welcome to Your Vue.js App"/>
    </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld.vue'
    import lottie from 'lottie-web';
    import Trophy from './JSON/data-1.json'

    export default {
        name: 'app',
        components: {
            HelloWorld
        },
        mounted() {
            lottie.loadAnimation({
                    container: this.$refs.animation,
                    renderer: 'canvas',
                    loop: true,
                    autoplay: true,
                    animationData: Trophy,//动画json
                }
            )
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
        margin-top: 60px;
    }
</style>
