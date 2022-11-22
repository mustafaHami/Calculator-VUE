<script>
import { track } from '@vue/reactivity';

    export default {
        props: {
            valClick: String
        }
    }
</script>

<template>
    <button class="btn">
        {{ valClick }}
    </button>
</template>