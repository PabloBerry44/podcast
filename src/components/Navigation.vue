<template>
    <nav>
        <div class="wrapper">
            <div class="inner">
                <img class="logo" src="../assets/logo.svg" alt="logo" />
                <ul v-if="state.wideDevice">
                    <li>Episodes</li>
                    <li>About</li>
                    <li>More</li>
                </ul>
            </div>

            <div class="button-wrapper" v-if="state.wideDevice">
                <Button class="light" name="RECENT EPISODES" />
                <Button class="dark" name="SUBSCRIBE" />
            </div>
            <img
                src="../assets/icons/menu-line.svg"
                alt="Menu"
                class="menu-icon"
                v-if="!state.wideDevice"
                @click="state.menu = !state.menu"
            />
        </div>
        <menu v-if="state.menu && !state.wideDevice">
            <ul>
                <li>Episodes</li>
                <li>About</li>
                <li>More</li>
                <Button class="light" name="RECENT EPISODES" />
                <Button class="dark" name="SUBSCRIBE" />
            </ul>
        </menu>
    </nav>
</template>

<script setup lang="ts">
import { reactive } from 'vue'
import Button from './Button.vue'

const state = reactive({
    menu: false,
    wideDevice: false,
})

window.addEventListener('resize', handleResize)

function handleResize() {
    if (window.innerWidth >= 1150) {
        state.wideDevice = true
    } else {
        state.wideDevice = false
    }
    console.log(window.innerWidth)
}

handleResize()
</script>

<style scoped lang="scss">
nav {
    background: var(--skinny);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    font-weight: bold;
    font-size: 16px;
    padding: 24px 10vw;

    @media (min-width: 1150px) {
        padding: 24px 140px;
    }

    .logo {
        width: 64px;
        cursor: pointer;
    }
    .menu-icon {
        width: 35px;
        cursor: pointer;
    }

    ul {
        justify-content: center;
        align-items: center;
        list-style-type: none;
        flex-direction: row;
        display: flex;
        gap: 60px;

        li {
            cursor: pointer;
        }
    }
    .wrapper {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        width: 100%;

        ul {
            flex-direction: row;
        }

        .inner {
            display: flex;
            gap: 124px;
        }

        .button-wrapper {
            display: flex;
            gap: 20px;
        }
    }

    menu {
        margin-top: 20px;

        ul {
            flex-direction: column;
            gap: 20px;
        }
    }
}
</style>
