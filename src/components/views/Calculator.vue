
<template>
    <div class="calculator">
        <div class="display">
            {{ current || 0 }}
        </div>
        <div @click="clear" class="btn">C</div>
        <div @click="sign()" class="btn operator">+/-</div>
        <div @click="persent('%')" class="btn operator">%</div>
        <div @click="append('/')" class="btn operator">/</div>
        <div @click="append('7')" class="btn">7</div>
        <div @click="append('8')" class="btn">8</div>
        <div @click="append('9')" class="btn">9</div>
        <div @click="append('*')" class="btn operator">*</div>
        <div @click="append('4')" class="btn">4</div>
        <div @click="append('5')" class="btn">5</div>
        <div @click="append('6')" class="btn">6</div>
        <div @click="append('-')" class="btn operator">-</div>
        <div @click="append('1')" class="btn">1</div>
        <div @click="append('2')" class="btn">2</div>
        <div @click="append('3')" class="btn">3</div>
        <div @click="append('+')" class="btn operator">+</div>
        <div @click="append('0')" class="btn zero">0</div>
        <div @click="dot()" class="btn">.</div>
        <div @click="equal()" class="btn operator">=</div>
        <div @click="" class="btn">History</div>
    </div>
</template>





<script>

export default {
    name: 'Calcilator',
    data() {
        return {
            current: '',
            operator: null,


        }
    },
    methods: {
        clear() {
            this.current = ''
        },
        sign(){
            this.current = this.current.charAt(0) === '-' ?
            this.current.slice(1) : '-${this.current}'
        },
        persent(){
            this.current = '${parseFloat(this.current)/100}'
        },
        append(number){
            this.current = '${this.current}${number}'
        },
        dot(){
            if(this.current.indexOf('.')===-1){
                this.append('.')
            }
        },
        equal(){
            this.current = eval(this.current)
        }
    }



}

</script>


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

.btn {
    background-color: #f2f2f2;
    border: 1px solid #999;
}

.zero {
    grid-column: 1/3;
}

.operator {
    background-color: orange;
    color: white;
}
</style>