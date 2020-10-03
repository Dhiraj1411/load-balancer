<template>
<div id="app">
    <navigation />
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <router-view></router-view> -->
    <globalScreen />
</div>
</template>

<script>
import navigation from "./components/core/navigation.vue";
import globalScreen from "./components/global.vue";
export default {
    name: "App",
    components: {
        navigation,
        globalScreen
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
