<template>
    <header>
        <h1 class="hero">Your Daily<br /><span>Podcast</span></h1>
        <p class="subtitle large">We cover all kinds of categories and a weekly special guest.</p>
        <Button name="SUBSCRIBE" class="dark shadow" />
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
            <img @click="changeTestimonial(true)" src="../assets/icons/arrow-right.svg" alt="LEFT" />
            <img @click="changeTestimonial(false)" src="../assets/icons/arrow-right.svg" alt="RIGHT" />
        </div>
    </section>

    <section class="features">
        <h2>Membership benefits</h2>
        <p class="large">Become our sponsor and get all benefits</p>
        <div class="feature-grid">
            <div class="feature">
                <img src="../assets/scribbles/scribble.svg" alt="scribble" />
                <p class="title">Topic by Request</p>
                <p class="text">Lorem ipsum dolor sit amet consectet pis cing elit, sed do eiusmod tempor.</p>
            </div>
            <div class="feature">
                <img src="../assets/scribbles/shining-stars.svg" alt="scribble" />
                <p class="title">Exclusive Content</p>
                <p class="text">Lorem ipsum dolor sit amet consectet pis cing elit, sed do eiusmod tempor.</p>
            </div>
            <div class="feature">
                <img src="../assets/scribbles/face-1.svg" alt="scribble" />
                <p class="title">Join the Community</p>
                <p class="text">Lorem ipsum dolor sit amet consectet pis cing elit, sed do eiusmod tempor.</p>
            </div>
            <div class="feature">
                <img src="../assets/scribbles/face-5.svg" alt="scribble" />
                <p class="title">Livestreaming Access</p>
                <p class="text">Lorem ipsum dolor sit amet consectet pis cing elit, sed do eiusmod tempor.</p>
            </div>
            <div class="feature">
                <img src="../assets/scribbles/fire.svg" alt="scribble" />
                <p class="title">Exclusive Episodes & Merch</p>
                <p class="text">Lorem ipsum dolor sit amet consectet pis cing elit, sed do eiusmod tempor.</p>
            </div>
            <div class="feature">
                <img src="../assets/scribbles/star.svg" alt="scribble" />
                <p class="title">And much more!</p>
                <p class="text">Lorem ipsum dolor sit amet consectet pis cing elit, sed do eiusmod tempor.</p>
            </div>
        </div>
        <Button name="SEE PRICING" class="dark shadow" />
    </section>

    <section class="episodes">
        <h2>Recent Episodes</h2>
        <p class="subtitle">Available on your favorite platform</p>

        <div class="episodes-grid">
            <div class="episode accent">
                <div class="main-content">
                    <img src="../assets/images/cover-1.webp" alt="episode cover" />
                    <div class="content">
                        <p class="medium">Eps. 6</p>
                        <p class="title">Pandemic Becoming Endemic</p>
                        <p class="description">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ac ultrices odio.
                        </p>
                    </div>
                </div>
                <div class="bottom">
                    <div class="hashtags">
                        <div class="hashtag">covid-19</div>
                        <div class="hashtag">health</div>
                    </div>
                    <div class="hosted-by">
                        <span>Hosted by:</span>
                        <img src="../assets/images/avatar-1.png" alt="lana" />
                        <img class="front" src="../assets/images/avatar-2.png" alt="lana" />
                    </div>
                </div>
            </div>
            <div class="episode">
                <div class="main-content">
                    <img src="../assets/images/cover-2.webp" alt="episode cover" />
                    <div class="content">
                        <p class="medium">Eps. 5</p>
                        <p class="title">Tesla Autopilot Controversy</p>
                        <p class="description">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ac ultrices odio.
                        </p>
                    </div>
                </div>
                <div class="bottom">
                    <div class="hashtags">
                        <div class="hashtag">automation</div>
                        <div class="hashtag">tech</div>
                    </div>
                    <div class="hosted-by">
                        <span>Hosted by:</span>
                        <img src="../assets/images/avatar-1.png" alt="lana" />
                        <img class="front" src="../assets/images/avatar-2.png" alt="lana" />
                    </div>
                </div>
            </div>
            <div class="episode">
                <div class="main-content">
                    <img src="../assets/images/cover-3.webp" alt="episode cover" />
                    <div class="content">
                        <p class="medium">Eps. 4</p>
                        <p class="title">Women's Rights? Is it alright?</p>
                        <p class="description">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ac ultrices odio.
                        </p>
                    </div>
                </div>
                <div class="bottom">
                    <div class="hashtags">
                        <div class="hashtag">women's rights</div>
                    </div>
                    <div class="hosted-by">
                        <span>Hosted by:</span>
                        <img src="../assets/images/avatar-1.png" alt="lana" />
                        <img class="front" src="../assets/images/avatar-2.png" alt="lana" />
                    </div>
                </div>
            </div>
            <div class="episode accent">
                <div class="main-content">
                    <img src="../assets/images/cover-4.webp" alt="episode cover" />
                    <div class="content">
                        <p class="medium">Eps. 3</p>
                        <p class="title">How to Deal with Self–Confidence</p>
                        <p class="description">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ac ultrices odio.
                        </p>
                    </div>
                </div>
                <div class="bottom">
                    <div class="hashtags">
                        <div class="hashtag">self-esteem</div>
                        <div class="hashtag">health</div>
                    </div>
                    <div class="hosted-by">
                        <span>Hosted by:</span>
                        <img src="../assets/images/avatar-1.png" alt="lana" />
                        <img class="front" src="../assets/images/avatar-2.png" alt="lana" />
                    </div>
                </div>
            </div>
            <div class="episode accent">
                <div class="main-content">
                    <img src="../assets/images/cover-5.webp" alt="episode cover" />
                    <div class="content">
                        <p class="medium">Eps. 2</p>
                        <p class="title">Type of Social Classes of People</p>
                        <p class="description">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ac ultrices odio.
                        </p>
                    </div>
                </div>
                <div class="bottom">
                    <div class="hashtags">
                        <div class="hashtag">social class</div>
                        <div class="hashtag">wealth</div>
                    </div>
                    <div class="hosted-by">
                        <span>Hosted by:</span>
                        <img src="../assets/images/avatar-1.png" alt="lana" />
                        <img class="front" src="../assets/images/avatar-2.png" alt="lana" />
                    </div>
                </div>
            </div>
            <div class="episode">
                <div class="main-content">
                    <img src="../assets/images/cover-6.webp" alt="episode cover" />
                    <div class="content">
                        <p class="medium">Eps. 1</p>
                        <p class="title">Are you a Perplexed Mind Person?</p>
                        <p class="description">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ac ultrices odio.
                        </p>
                    </div>
                </div>
                <div class="bottom">
                    <div class="hashtags">
                        <div class="hashtag">mind-behaviour</div>
                        <div class="hashtag">health</div>
                    </div>
                    <div class="hosted-by">
                        <span>Hosted by:</span>
                        <img src="../assets/images/avatar-1.png" alt="lana" />
                        <img class="front" src="../assets/images/avatar-2.png" alt="lana" />
                    </div>
                </div>
            </div>
        </div>
        <Button class="dark shadow" name="BROWSE ALL EPISODES" />
    </section>

    <Footer />
</template>

<script setup lang="ts">
import Button from '../components/Button.vue'
import Footer from '../components/Footer.vue'
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
    margin-top: 140px;
    padding-bottom: 100px;

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
        height: 420px;
        align-items: center;
        position: relative;
        justify-content: center;

        .testimonial {
            background: white;
            padding: 40px;
            width: 350px;
            display: flex;
            flex-direction: column;
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

    .arrows {
        img {
            cursor: pointer;

            &:first-child {
                transform: rotateZ(180deg);
            }
        }
    }
}

.features {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    padding: 10px;
    text-align: center;

    h2 {
        margin-top: 140px;
        margin-bottom: 20px;
        font-weight: 700;
    }
    .feature-grid {
        display: grid;
        max-width: max-content;
        margin-top: 100px;
        gap: 40px;

        @media (min-width: 1000px) {
            grid-template-columns: repeat(2, 1fr);
        }
        @media (min-width: 1400px) {
            grid-template-columns: repeat(3, 1fr);
        }

        .feature {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            width: 100%;
            max-width: 373px;
            text-align: center;

            .title {
                font-size: 22px;
                font-weight: 700;
                margin-top: 30px;
            }

            .text {
                font-size: 16px;
                font-weight: 500;
                margin-top: 10px;
            }
        }
    }
    button {
        margin-top: 100px;
        margin-bottom: 140px;
    }
}

.episodes {
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    background: var(--skinny);
    padding: 15px;

    h2 {
        margin-top: 140px;
    }
    .subtitle {
        margin-top: 20px;
    }

    .episodes-grid {
        display: grid;
        gap: 20px;
        margin-top: 100px;

        @media (min-width: 1000px) {
            grid-template-columns: repeat(2, 1fr);
        }

        .episode {
            display: flex;
            flex-direction: column;
            padding: 16px;
            border: 2px solid black;
            border-radius: 12px;
            max-width: 570px;
            background: white;
            width: 100%;

            &.accent {
                .title {
                    color: var(--red);
                }
                -webkit-box-shadow: 10px 9px 0px 0px rgba(129, 173, 200, 1);
                -moz-box-shadow: 10px 9px 0px 0px rgba(129, 173, 200, 1);
                box-shadow: 10px 9px 0px 0px rgba(129, 173, 200, 1);
            }

            .main-content {
                display: flex;
                flex-direction: column;
                gap: 20px;

                img {
                    width: 100%;
                }

                @media (min-width: 600px) {
                    flex-direction: row;

                    img {
                        max-width: 166px;
                    }
                }

                .content {
                    display: flex;
                    flex-direction: column;

                    .medium {
                        font-size: 16px;
                        font-weight: 700;
                        color: var(--red);
                        margin-top: 17.5px;
                    }

                    .title {
                        font-size: 22px;
                        font-weight: 700;
                        margin-top: 4px;
                    }

                    .description {
                        font-size: 14px;
                        font-weight: 500;
                        margin-top: 15px;
                        border-top: 1px solid gray;
                        padding-top: 10px;
                    }
                }
            }

            .bottom {
                margin-top: 20px;
                display: flex;
                flex-flow: row wrap;
                justify-content: space-between;
                gap: 15px;

                .hashtags {
                    display: flex;
                    flex-direction: row;
                    gap: 6px;

                    .hashtag {
                        padding: 6px 12px;
                        font-size: 12px;
                        font-weight: 500;
                        color: gray;
                        border: 1px solid gray;
                        border-radius: 4px;
                    }
                }

                .hosted-by {
                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    font-size: 12px;
                    font-weight: 700;
                    color: rgb(94, 94, 94);

                    img {
                        border-radius: 50%;
                        &:first-of-type {
                            margin-left: 10px;
                        }

                        &.front {
                            transform: translateX(-7px);
                            border: 2px solid white;
                        }
                    }
                }
            }
        }
    }

    button {
        margin-top: 100px;
        margin-bottom: 140px;
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
