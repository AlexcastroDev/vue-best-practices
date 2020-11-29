<template>
    <div>
        <span>{{msg}} </span>
        <p>vmodel: {{modelValue}}</p>
        <p><button @click="close()">Click to Close</button></p>
    </div>
</template>

<script>
export default {
    name: "Dialog",
    props: {
        modelValue: {
            required: true,
            type: Boolean
        },
        msg: {
            type: String,
            required: false,
            default: () => "Nothing..."
        }
    },
    methods: {
        close() {
            this.$emit('update:modelValue', false)
        }
    }
}
</script>