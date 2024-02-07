<script>

export default {
    name: "FooterBottom",
    data() {
        return {
            ArraySocialIcons: [
                {
                    link: '#',
                    icon: 'footer-facebook.png',
                },
                {
                    link: '#',
                    icon: 'footer-twitter.png',
                },
                {
                    link: '#',
                    icon: 'footer-youtube.png',
                },
                {
                    link: '#',
                    icon: 'footer-pinterest.png',
                },
                {
                    link: '#',
                    icon: 'footer-periscope.png',
                }
            ]
        }
    }
}

</script>

<template>
    <footer>

        <div class="container">

            <div>
                <button>Sign-up now!</button>
            </div>

            <div class="socials">
                <h3>Follow us</h3>
                <ul>
                    <li v-for=" (element, index) in ArraySocialIcons" :key="index">
                        <a href="element.link">
                            <img :src="`./src/assets/img/${element.icon}`" alt="Social Icon" width="30">
                        </a>
                    </li>
                </ul>
            </div>

        </div>

    </footer>
</template>

<style lang="scss" scoped>
@use '../style/general' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;

footer {

    background-color: $footer-color;
    padding-block: 40px;

    .container {
        width: 80%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;

        button {
            border: 2px solid $accent-color;
            background-color: rgba(0, 0, 0, 0);
            color: white;
            padding: 10px 20px;
            font-size: 1rem;
            text-transform: uppercase;
            cursor: pointer;
        }

        .socials {
            display: flex;
            gap: 30px;
            align-items: center;

            h3 {
                color: $accent-color;
                text-transform: uppercase;
                font-size: 1.5rem;
                font-weight: 700;
            }

            ul {
                display: flex;
                gap: 20px;

                li {
                    list-style: none;
                }
            }
        }
    }
}
</style>