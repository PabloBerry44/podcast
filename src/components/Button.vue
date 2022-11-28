<template>
    <button>{{ props.name }}</button>
</template>
<script setup lang="ts">
const props = defineProps<{
    name?: string
    disabled?: boolean
}>()
</script>
<style scoped lang="scss">
button {
    padding: 12px 24px;
    border: 2px solid black;
    border-radius: 8px;
    font-weight: bold;
    font-size: 14px;
    cursor: pointer;
}
.light {
    background: transparent;
}
.dark {
    background: black;
    color: white;
}
</style>
