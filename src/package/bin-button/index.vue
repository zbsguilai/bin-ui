<template>
    <button @click="handleClick" :disabled='disabled'>
        <slot></slot>
    </button>
</template>
<script>
export default {
    name: "BinButton",
    props: {
        disabled: Boolean
    },
    methods: {
        handleClick(evt) {
            this.$emit('click', evt);
        }
    }
};
</script>
