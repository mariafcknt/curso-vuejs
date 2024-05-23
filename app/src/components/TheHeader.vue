<template>
    <header class="header">
        Header
    </header>
</template>

<script>
    export default {
        beforeUnmount() {
            console.log("beforeUnmount");
        },
        unmounted() {
            console.log("unmounted");
        },
    }
</script>

<style>
    .header {
        background: black;
        color: #fff;
        padding: 5px;
    }
</style>