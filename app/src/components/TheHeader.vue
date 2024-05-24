<template>
    <header class="header">
        
        <h1 
            v-if="$slots.title"
            class="title">
            <slot name="title" />
        </h1>

        <div class="description">
            <slot name="description"></slot>
        </div>

        <div class="content">
            <slot></slot>
        </div>
    </header>
</template>

<script>
    export default {
        mounted() {
            console.log(this.$slots)
        }
    }
</script>

<style>
    .header {
        background: black;
        color: #fff;
    }
</style>