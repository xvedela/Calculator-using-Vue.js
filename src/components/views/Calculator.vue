<script>


export default {
    name: 'Calcilator'



}

</script>


<template>
<div class="calculator">
    <div class="display">
        {{ current || 0}}
    </div>
    <div class="btn">C</div>
    <div class="btn">+/-</div>
    <div class="btn">%</div>
    <div class="btn">/</div>
    <div class="btn">7</div>
    <div class="btn">8</div>
    <div class="btn">9</div>
    <div class="btn">*</div>
    <div class="btn">4</div>
    <div class="btn">5</div>
    <div class="btn">6</div>
    <div class="btn">-</div>
    <div class="btn">1</div>
    <div class="btn">2</div>
    <div class="btn">3</div>
    <div class="btn">+</div>
    <div class="btn">0</div>
    <div class="btn">.</div>
    <div class="btn">=</div>
</div>

</template>


<style>
.calculator {
    cursor: pointer;
    width: 400px;
    font-size: 40px;
    display: grid;
    margin: 0 auto;
    grid-template-columns: repeat(4, 1fr);
    grid-auto-rows: minmax(50px, auto);
}
.display {
    grid-column: 1/5;
    background-color: #333;
    color: white;
}


</style>