<template>
    <div :class="baseClass">
        {{ test }}
        <slot />
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
    padding: 10px;
    border-radius: 6px;
    color: gray;
    background: #ddd;
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
