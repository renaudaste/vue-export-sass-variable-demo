<template>
    <div id="app">
        <img alt="Vue logo" height="100px" src="./assets/logo.png">
        <home/>
    </div>
</template>

<script>
    import Home from './components/home.component'

    export default {
        name: 'app',
        components: {Home}
    }
</script>

<style lang="scss">

    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        img {
            margin: 1rem 0;
        }
    }

    body {
        background-color: #EEE;
    }
</style>
