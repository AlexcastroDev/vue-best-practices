<template>
        <p><button @click="open()">Click to show</button></p>
        <dialog-component 
        v-model="dialog"
        msg="Welcome to Your Vue.js App"
        @update:modelValue="dialog = $event"
        />
</template>

<script>
import DialogComponent from './dialog'
export default {
    name: "Dialog",
    components: {DialogComponent},
    data: () => ({
        dialog: false
    }),
    methods: {
        open() {
            this.dialog = true
        }
    }
}
</script>