<template>
    <button @click="clickEvent">
        按钮
    </button>
</template>
<script lang="ts">
    import {
        Vue,
        Component,
        Prop,
        Emit
    } from 'vue-property-decorator';
    @Component
    export default class Button extends Vue {
        @Prop(String) private type!: string
        @Prop(Boolean) private primary: boolean

        @Emit('click')
        private emitClick(event: MouseEvent) {

        }
        private clickEvent(event: MouseEvent) {
            this.emitClick(event);
        }
        private created() {
            console.log(this.type, this.primary);
        }
    }
</script>