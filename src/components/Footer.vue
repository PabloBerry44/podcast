<template>
    <footer>
        <div class="footer-inner">
            <div class="column-left">
                <img class="logo" src="../assets/logo.svg" alt="POD OF CAST" />
                <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span>
                <div class="social-icon-row">
                    <img src="../assets/icons/black-twitter.svg" alt="twitter" />
                    <img src="../assets/icons/black-instagram.svg" alt="twitter" />
                    <img src="../assets/icons/black-tiktok.svg" alt="twitter" />
                </div>
            </div>
            <div class="menu">
                <div class="column">
                    <router-link class="link" to="">About</router-link>
                    <router-link class="link red" to="">Testimonials</router-link>
                    <router-link class="link" to="">Features</router-link>
                </div>
                <div class="column">
                    <router-link class="link red" to="">Episodes</router-link>
                    <router-link class="link" to="">Pricing</router-link>
                    <router-link class="link" to="">Blog</router-link>
                </div>
            </div>
            <div class="platforms-wrapper">
                <div class="platforms">
                    <p class="large">Listen to episodes on your fav platform:</p>
                    <div class="platform-row">
                        <img src="../assets/icons/google-podcasts.svg" alt="Google Podcasts" />
                        <img src="../assets/icons/spotify.svg" alt="Spotify" />
                        <img src="../assets/icons/youtube.svg" alt="YouTube" />
                    </div>
                </div>
                <div class="platforms">
                    <p class="large">App available on:</p>
                    <div class="platform-row large">
                        <img src="../assets/icons/app_store.webp" alt="Google Podcasts" />
                        <img src="../assets/icons/google_play.webp" alt="Spotify" />
                    </div>
                </div>
            </div>
        </div>
        <div class="bottom-line"></div>
        <div class="bottom-row">
            <p>©2022. All Rights Reserved. <span>Pod of Cast</span></p>
            <ul>
                <li>Terms</li>
                •
                <li>Privacy</li>
            </ul>
        </div>
    </footer>
</template>

<style scoped lang="scss">
footer {
    display: flex;
    padding: 10vw;
    flex-direction: column;
    .footer-inner {
        width: 100%;
        display: flex;
        flex-flow: row wrap;
        gap: 60px;

        @media (min-width: 1250px) {
            justify-content: space-between;
        }
    }

    .column-left {
        display: flex;
        flex-direction: column;
        max-width: 275px;
        gap: 40px;

        .logo {
            width: 74px;
        }
        span {
            font-size: 14px;
            font-weight: 500;
        }
        .social-icon-row {
            display: flex;
            flex-flow: row nowrap;
            gap: 25px;

            img {
                width: 24px;
            }
        }
    }

    .menu {
        display: flex;
        flex-flow: row nowrap;
        gap: 93px;
        font-size: 16px;
        font-weight: 500;

        .column {
            display: flex;
            flex-direction: column;
            gap: 20px;

            .link {
                text-decoration: none;
                color: initial;

                &.red {
                    color: var(--red);
                }
            }
        }
    }

    .platforms-wrapper {
        display: flex;
        flex-direction: column;
        gap: 60px;

        .platforms {
            display: flex;
            flex-direction: column;
            gap: 30px;

            .platform-row {
                display: flex;
                flex-flow: row wrap;
                gap: 38px;

                &.large {
                    gap: 20px;

                    img {
                        height: 36px;
                    }
                }

                img {
                    height: 22px;
                }
            }
        }
    }

    .bottom-line {
        width: 100%;
        height: 2px;
        background: lightgray;
        margin-top: 140px;
    }

    .bottom-row {
        margin-top: 20px;
        display: flex;
        flex-flow: row wrap;
        justify-content: space-between;
        gap: 20px;

        span {
            color: var(--red);
        }

        ul {
            list-style: none;
            display: flex;
            flex-direction: row;
            gap: 10px;
        }
    }
}
</style>
