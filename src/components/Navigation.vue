<template>
    <nav>
        <div class="wrapper">
            <img src="../assets/logo.svg" alt="logo" />
            <p @click="state.menuVisible = !state.menuVisible">menu</p>
        </div>
        <menu v-if="state.menuVisible">
            <ul>
                <li>Episodes</li>
                <li>About</li>
                <li>More</li>
            </ul>
        </menu>
    </nav>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const state = ref({
    menuVisible: false,
})
</script>

<style scoped lang="scss">
nav {
    background: var(--skinny);
    padding: 24px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    img {
        width: 64px;
    }
    .wrapper {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        width: 100%;
    }

    menu {
        margin-top: 20px;

        ul {
            list-style-type: none;
            flex-direction: column;
            display: flex;
            gap: 20px;
        }
    }
}
</style>
