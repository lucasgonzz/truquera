<template>
    <div id="app" :style="image">
        <truquera></truquera>
    </div>
</template>

<script>
import Truquera from '@/components/Truquera'
import fondo from '@/assets/fondo-madera.jpg'
export default {
    name: 'App',
    components: {
        Truquera
    },
    data() {
        return {
            image: {backgroundImage: `url(${fondo})`}
        }
    }
}
</script>

<style lang="sass">
@import "./sass/fonts/styles.css"
[class^='icon-']:before
    position: relative
    top: .2em
    // margin-right: .1em
#app  
    font-family: Avenir, Helvetica, Arial, sans-serif
    -webkit-font-smoothing: antialiased
    -moz-osx-font-smoothing: grayscale
    text-align: center
    color: #2c3e50
    height: 100vh
    background-repeat: space

</style>
