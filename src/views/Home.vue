<template>
    <header>
        <div class="hero">Your Daily<br /><span>Podcast</span></div>
        <p class="subtitle large">We cover all kinds of categories and a weekly special guest.</p>
        <Button name="SUBSCRIBE" class="dark" />
        <section class="covers">
            <img src="../assets/images/cover-1.webp" alt="empty-alt" />
            <img src="../assets/images/cover-2.webp" alt="empty-alt" />
            <img src="../assets/images/cover-3.webp" alt="empty-alt" />
            <img src="../assets/images/cover-4.webp" alt="empty-alt" />
            <img src="../assets/images/cover-5.webp" alt="empty-alt" />
        </section>
        <section class="platforms">
            <p>Supported by:</p>
            <img src="../assets/icons/spotify.svg" alt="Spotify" />
            <img src="../assets/icons/google-podcasts.svg" alt="Google Podcasts" />
            <img src="../assets/icons/youtube.svg" alt="YouTube" />
        </section>
        <img class="loop" src="../assets/scribbles/loop.svg" alt="empty-alt" />
    </header>
    <section class="about">
        <h1>Talk. Listen. Get inspired by every minute of it.</h1>
        .
    </section>
</template>

<script setup lang="ts">
import Button from '../components/Button.vue'
</script>

<style scoped lang="scss">
header {
    display: flex;
    flex-direction: column;
    align-items: center;
    background: var(--skinny);

    .hero {
        font-size: 76px;
        text-align: center;
        margin-top: 64px;

        span {
            color: var(--red);
        }

        @media (min-width: 600px) {
            font-size: 96px;
        }
    }
    .subtitle {
        margin-top: 40px;
        color: var(--grey);
        max-width: 300px;
        text-align: center;
    }

    button {
        margin-top: 60px;
        padding: 24px 48px;

        box-shadow: 6px 6px 0px rgba(0, 0, 0, 0.192);
    }

    .covers {
        overflow: hidden;
        display: flex;
        gap: 20px;
        max-width: 100%;
        justify-content: center;
        margin-top: 120px;

        img {
            width: 90%;
            min-width: 300px;
            max-width: 373px;
        }
    }
    .platforms {
        margin-top: 120px;
        margin-bottom: 140px;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 50px;
        border-top: 2px solid var(--grey);
        border-bottom: 2px solid var(--grey);
        padding: 45px 45px 45px 0;

        img {
            height: 40px;
        }

        p {
            min-width: max-content;
            font-size: 23px;
            font-weight: bold;
        }

        @media (min-width: 1200px) {
            flex-direction: row;
            gap: 100px;

            img {
                height: 32px;
            }
        }
    }
    .loop {
        transform: translateY(50%);
    }
}
.about {
    text-align: center;
    display: flex;
    justify-content: center;
    width: 100%;

    h1 {
        margin-top: 140px;
        max-width: 780px;
    }
}
</style>
