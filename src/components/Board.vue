<script>
    import Button from './Button.vue';
    export default {
        data() {
            return {
                values1 : ["C","PI","%","AC"],
                values2 : ["7","8","9","x"],
                values3 : ["4","5","6","÷"],
                values4 : ["1","2","3","-"],
                values5 : ["0",".","=","+"],
                val : ''
            }
        },
        props: {
            result : this.val
        },
        components: {
            Button
        },
        methods: {
            calcule(e){
                alert(e)
                this.val += e
            }
            
        }
    }
  
</script>

<template>
    <div >
        <Button class="btn" v-for="value in values1" :valClick="value" @click="calcule(value)"/>
    </div>
    <div >
        <Button class="btn" v-for="value in values2" :valClick="value" @click="calcule(value)"/>
    </div>
    <div >
        <Button class="btn" v-for="value in values3" :valClick="value" @click="calcule(value)"/>
    </div>
    <div >
        <Button class="btn" v-for="value in values4" :valClick="value" @click="calcule(value)"/>
    </div>
    <div >
        <Button class="btn" v-for="value in values5" v-if="value = '='" :valClick="value" @click="calcule(value)"/>
    </div>
</template>