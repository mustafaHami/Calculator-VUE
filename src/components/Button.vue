<script>
import { track } from '@vue/reactivity';

    export default {
        props: {
            valClick: String
        },
        // emits:['value'],
        // created() {
        //     this.$emit('value',)
        // }
    }
</script>

<template>
    <button>
        {{ valClick }}
    </button>
</template>