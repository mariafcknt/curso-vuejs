<template>
    <div :class="baseClass">
        Seu formulário foi enviado com sucesso!
    </div>
</template>

<script>

export default {
    props: ['variant'],
    computed: {
        baseClass() {
            
        }
    }
}

</script>

<style scoped>

.alert {
    padding: 5px;
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
