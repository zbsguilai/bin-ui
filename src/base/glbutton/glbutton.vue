<template>
    <button @click="handleClick" :disabled='disabled'>
        <slot></slot>
    </button>
</template>

<script>

export default {
    name: "GlButton",
    props: {
        disabled: Boolean
    },
    components: {
        HelloWorld,
    },
    methods: {
        handleClick(evt) {
            this.$emit('click', evt);
        }
    }
};
</script>
