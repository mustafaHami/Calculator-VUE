<script>
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
    methods: {
      calcule(e) {
        if(e === '=') {
          const result = eval(this.val)
          this.val = result.toPrecision(3)
        }else if (e === 'C'){
          const result = this.val.slice(0, this.val.length - 1)
          this.val = result
        }else if (e === 'AC'){
          this.val = ''
        }else if (e === 'x'){
          this.val += '*'
        }else if (e === '÷'){
          this.val+= '/'
        }else if (e === 'PI'){
          const result = this.val.slice(0, this.val.length - 1)
          this.val += Math.PI.toPrecision(3)
        }else{
          this.val += e
        }
        

      }
    }
  }

</script>

<template>
<div class="container">
  <div class="resultat">
    <p>{{val}}</p>
  </div>
  <div class="clavier">
    <div >
        <button class="btn" v-for="value in values1"  @click="calcule(value)">
          {{value}}
        </button>
    </div>
    <div >
        <button class="btn" v-for="value in values2" @click="calcule(value)">
          {{value}}
        </button>
    </div>
    <div >
        <button class="btn" v-for="value in values3"  @click="calcule(value)">
          {{value}}
        </button>
    </div>
    <div >
        <button class="btn" v-for="value in values4"  @click="calcule(value)">
          {{value}}
        </button>
    </div>
    <div >
        <button class="btn" v-for="value in values5"   @click="calcule(value)">
          {{value}}
        </button>
    </div>
  </div>
</div>
</template>

