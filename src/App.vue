<script>
import Calculator from "./components/views/Calculator.vue"

export default {
    name: "app",
    components: {
        Calculator
    }
};
</script>

<template>
    <div id="app">
        <Calculator />
    </div>
</template>

<style>
#app {
    font-family: "Avenir", Arial, Helvetica, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    margin-top: 30px;
    color: #2c3e50;
}
</style>

