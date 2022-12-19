<template>
    <header>
        <h1 class="hero">Your Daily<br /><span>Podcast</span></h1>
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
        <h2>Talk. Listen. Get inspired by every minute of it.</h2>
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
        <h3>One of the best daily podcasts that covers every topic on Spotify.</h3>
        <p>Social Community Manager at Spotify</p>
    </section>

    <section class="testimonials">
        <h2>What our listeners say</h2>
        <p class="large subtitle">Their experience throughout every platform</p>
        <div class="container">
            <Transition :name="carouselState.transitionName">
                <div class="testimonial" v-if="carouselState.currentTestimonial == 0">
                    <p class="text">
                        Lorem ipsum dolor sit amet consectet piscing elit, sed do eiusmod tempor incidi ut labore et
                        dolore magna aliqua.
                    </p>
                    <div class="person-row">
                        <img class="person-image" src="../assets/images/luna.webp" alt="person image" />
                        <span class="name">Luna lovegood,</span>
                        <img class="company-logo" src="../assets/icons/spotify.svg" alt="spotify logo" />
                    </div>
                </div>
                <div class="testimonial" v-else-if="carouselState.currentTestimonial == 1">
                    <p class="text">
                        Lorem ipsum dolor sit amet consectet piscing elit, sed do eiusmod tempor incidi ut labore et
                        dolore magna aliqua.
                    </p>
                    <div class="person-row">
                        <img class="person-image" src="../assets/images/emily.webp" alt="person image" />
                        <span class="name">Emily Blunt,</span>
                        <img
                            class="company-logo"
                            src="../assets/icons/google-podcasts.svg"
                            alt="google podcasts logo"
                        />
                    </div>
                </div>
                <div class="testimonial" v-else-if="carouselState.currentTestimonial == 2">
                    <p class="text">
                        Lorem ipsum dolor sit amet consectet piscing elit, sed do eiusmod tempor incidi ut labore et
                        dolore magna aliqua.
                    </p>
                    <div class="person-row">
                        <img class="person-image" src="../assets/images/mia.webp" alt="person image" />
                        <span class="name">Mia Winters,</span>
                        <img class="company-logo" src="../assets/icons/youtube.svg" alt="youtube logo" />
                    </div>
                </div>
            </Transition>
        </div>

        <div class="arrows" style="display: flex; gap: 30px; margin-top: 50px">
            <div class="arrow-left" @click="changeTestimonial(true)">LEFT</div>
            <div class="arrow-right" @click="changeTestimonial(false)">RIGHT</div>
        </div>
    </section>

    <div class="es" style="height: 300px"></div>
</template>

<script setup lang="ts">
import Button from '../components/Button.vue'
import { reactive } from 'vue'

const carouselState = reactive({
    currentTestimonial: 0,
    transitionName: 'slide-right',
})

function changeTestimonial(next: boolean) {
    if (next) {
        carouselState.transitionName = 'slide-right'
        if (carouselState.currentTestimonial == 2) {
            carouselState.currentTestimonial = 0
        } else {
            carouselState.currentTestimonial++
        }
    } else {
        carouselState.transitionName = 'slide-left'
        if (carouselState.currentTestimonial == 0) {
            carouselState.currentTestimonial = 2
        } else {
            carouselState.currentTestimonial--
        }
    }
}
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
        font-weight: 500;
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

    h2 {
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

    h3 {
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

    p {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: center;
        gap: 10px;
        margin-top: 40px;
        text-align: center;
    }
}

.testimonials {
    background: var(--blueish);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    h2 {
        margin-top: 140px;
    }
    .subtitle {
        margin-top: 20px;
    }

    .container {
        margin-top: 100px;
        display: flex;
        flex-direction: row;
        gap: 5vw;
        overflow-x: hidden;
        width: 100%;
        height: 300px;
        align-items: center;

        .testimonial {
            background: white;
            padding: 40px;
            min-width: 90vw;
            display: flex;
            flex-direction: column;
            margin-left: 5vw;
            position: absolute;

            .text {
                position: relative;
                margin-top: 92px;
                font-size: 22px;
                font-weight: 500;

                &::before {
                    content: '“';
                    position: absolute;
                    transform: translateY(-75%);
                    font-size: 96px;
                    color: var(--red);
                    font-weight: 600;
                }
            }

            .person-row {
                margin-top: 32px;
                display: flex;
                flex-direction: row;
                align-items: center;
                gap: 10px;

                .person-image {
                    width: 48px;
                }
                .company-logo {
                    height: 22px;
                }
            }
        }
    }
}

.slide-right-enter-active,
.slide-right-leave-active {
    transition: all 0.25s ease-out;
}
.slide-right-enter-from {
    opacity: 0;
    transform: translateX(-100%);
}
.slide-right-leave-to {
    opacity: 0;
    transform: translateX(100%);
}

.slide-left-enter-active,
.slide-left-leave-active {
    transition: all 0.25s ease-out;
}
.slide-left-enter-from {
    opacity: 0;
    transform: translateX(100%);
}
.slide-left-leave-to {
    opacity: 0;
    transform: translateX(-100%);
}
</style>
