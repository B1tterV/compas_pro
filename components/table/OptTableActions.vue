<template>
    <div class="opt-table-actions">
        <div
            v-for="(action, actionIndex) in actions"
            :key="`action-${actionIndex}`"
            class="opt-table-actions__action-item"
        >
            {{ action.name }}
        </div>
    </div>
</template>

<script setup lang="ts">
import { useTableStore } from '~/store/table'
const { actions } = storeToRefs(useTableStore())

defineProps({
  rowIndex: { type: Number, required: true }
})
</script>

<style scoped lang="scss">
.opt-table-actions{
    position: absolute;
    top: -10px;
    left: 10px;
    border-radius: 5px;
    border: solid 1px #eeeff1;
    background-color: #fbfcfd;
    color: #ae0a0a;
    &__action-item{
        padding: 5px 15px;
        &:hover{
            background-color: #eef3f8;
        }
    }
}
</style>
