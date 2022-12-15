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
        <div class="columns-container">
            <div class="column">
                <img src="../assets/scribbles/thought.svg" alt="" />
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ac ultrices odio.</p>
            </div>
            <div class="column">
                <img src="../assets/scribbles/bulb.svg" alt="" />
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ac ultrices odio.</p>
            </div>
        </div>
    </section>
    <section class="quote">
        <h2>One of the best daily podcasts that covers every topic on Spotify.</h2>
        <div class="row">
            <img class="avatar" src="../assets/images/avatar.webp" alt="avatar" />
            John Smith,
            <div class="wrapper">
                <img class="spotify" src="../assets/icons/spotify-black.svg" alt="Spotify" />
                <p>Social Community Manager</p>
            </div>
        </div>
    </section>
    <p>whatever</p>
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
    align-items: center;
    width: 100%;
    flex-direction: column;
    padding: 20px;

    h1 {
        margin-top: 140px;
        max-width: 780px;
    }

    .columns-container {
        display: flex;
        flex-direction: column;
        margin-top: 100px;
        gap: 100px;

        @media (min-width: 1200px) {
            flex-direction: row;
        }

        .column {
            max-width: 450px;

            img {
                width: 80%;
                max-width: 275px;
            }
        }
    }
}
.quote {
    margin-inline: auto;
    width: 90%;
    max-width: 1160px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 120px;
    padding: 40px;
    background: var(--skinny);
    flex-direction: column;

    h2 {
        max-width: 650px;
        text-align: center;
        margin-top: 100px;

        &::before {
            content: '“';
            position: absolute;
            left: 50%;
            transform: translate(-50%, -150%);
            font-size: 96px;
            color: var(--red);
        }
    }
    .row {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: center;
        gap: 10px;
        margin-top: 40px;

        .wrapper {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        p {
            font-weight: bold;
        }

        .avatar {
            width: 48px;
        }
        .spotify {
            width: 30px;
            display: inline-block;
        }
    }
}
</style>
