<template>
<Button @click="fn"></Button>
</template>
<script lang="ts">
    import Button from '@/components/Button.vue';
    import {
        Component,
        Vue
    } from 'vue-property-decorator';
    //Button注册到这个组件上面来
    @Component({
        components: {
            Button
        }
    })
    export default class Index extends Vue {
        private fn(event: MouseEvent) {
            console.log(1)
        }
    }
</script>