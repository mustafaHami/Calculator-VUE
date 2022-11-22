<script>
  import Board from './Board.vue';
  
  export default {
    data() {
        return {
            result : "",
        }
    },
    components: {
      Board
    },
  }

</script>

<template>
  <div class="container">
    <div class="resultat">
        <p>{{result}}</p>
    </div>
    <div class="clavier">
        <Board @response="(msg) => result = msg"/>
    </div>
  </div>
    
</template>