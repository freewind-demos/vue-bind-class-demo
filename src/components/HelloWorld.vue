<template>
    <div class="hello" v-bind:class="{ red: enableRed(), green: enableGreen() }">
        {{ msg }}
    </div>
</template>

<script lang="ts">
    import {Component, Prop, Vue} from 'vue-property-decorator';

    @Component
    export default class HelloWorld extends Vue {
        @Prop() private msg: string = "Hello Vue!";

        enableRed() {
            return false
        }

        enableGreen() {
            return true
        }
    }
</script>

<style scoped>
    .hello {
        background-color: #EEE;
    }

    .red {
        color: red;
    }

    .green {
        color: green;
    }
</style>
