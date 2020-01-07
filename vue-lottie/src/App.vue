<template>
    <div id="app">
        <div class="animation-style" ref="animation"></div>
    </div>
</template>

<script>
    import lottie from 'lottie-web';
    import Trophy from './JSON/13667-new-year-2020.json'

    export default {
        name: 'app',
        components: {

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

</style>
