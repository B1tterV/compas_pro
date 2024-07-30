<template>
    <div class="opt-sidebar" />
</template>

<script setup lang="ts">

</script>

<style scoped>
.opt-sidebar{
    background-color: #1b2735;
    height: 100vh;
    min-width: 240px;
}

@media (max-width: 720px){
    .opt-sidebar{
        display: none;
    }
}
</style>
