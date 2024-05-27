<template>
    <div :class="baseClass">
        <slot />
        <button @click="onClick()">
            X
        </button>
    </div>
</template>

<script>

export default {
    props: {
        variant: {
            type: String,
            default: ''
        },
        test: {
            type: String,
            default: 'test'
        },
    },

    methods: {
        onClick() {
            this.$emit('close')
            console.log('clicou');
        }
    },

    computed: {
        baseClass() {
            return [
                'alert',
                this.variant ? `alert-${this.variant}` : '']
        }
    }
}

</script>

<style scoped>

.alert {
    display: flex;
    justify-content: space-between;
    padding: 10px;
    border-radius: 6px;
    color: gray;
    background: #ddd;
}

.alert > button {
    color: white;
    background-color: #42b983;
    border-radius: 20px;
    padding-right: 15px;
    padding-left: 15px;
    border: 1px solid white;
    cursor: pointer;
}

.alert > button:hover {
    background-color: #2e805b;
}

.alert-success {
    background: #42b983;
    color: white;
}

.alert-danger {
    background: red;
    color: white
}

</style>
