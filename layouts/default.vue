<template>
    <div class="page-layout">
        <div class="page-layout__content">
            <opt-sidebar />

            <div class="page">
                <slot />
            </div>
        </div>
    </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.page-layout{
    overflow: hidden;
    height: 100vh;
    &__content{
        height: 100vh;
        display: flex;
        .page{
            padding: 20px;
            max-width: calc(100% - 250px);
            width: 100%;
            overflow: auto;
        }
    }
}

@media (max-width: 720px){
    .page-layout{
    overflow: hidden;
    height: 100vh;
    &__content{
        height: 100vh;
        display: flex;
        .page{
            max-width: 100%;
            width: 100%;
        }
    }
}
}
</style>
