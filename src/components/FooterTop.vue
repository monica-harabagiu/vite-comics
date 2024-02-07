<script>

export default {
    name: "FooterTop",
    data() {
        return {
            ArrayIconLinks: [
                {
                    name: 'Digital comics',
                    link: '#',
                    icon: 'buy-comics-digital-comics.png',
                    width: '40'
                },
                {
                    name: 'DC merchandise',
                    link: '#',
                    icon: 'buy-comics-merchandise.png',
                    width: '50'
                },
                {
                    name: 'Subscription',
                    link: '#',
                    icon: 'buy-comics-subscriptions.png',
                    width: '50'
                },
                {
                    name: 'Comic shop locator',
                    link: '#',
                    icon: 'buy-comics-shop-locator.png',
                    width: '30'
                },
                {
                    name: 'DC power visa',
                    link: '#',
                    icon: 'buy-dc-power-visa.svg',
                    width: '50'
                }
            ]
        }
    }
}

</script>

<template>
    <footer>
        <div>
            <ul>
                <li v-for=" (element, index) in ArrayIconLinks" :key="index">
                    <img :src="`./src/assets/img/${element.icon}`" alt="" :width="element.width">
                    <a href="element.link">{{ element.name }}</a>
                </li>
            </ul>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../style/general' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;

footer {

    background-color: $accent-color;
    padding-block: 50px;

    div {

        width: 75%;
        margin: 0 auto;

        ul {

            display: flex;
            justify-content: space-around;

            li {
                list-style: none;
                display: flex;
                gap: 20px;
                align-items: center;

                a {
                    text-decoration: none;
                    color: white;
                    text-transform: uppercase;
                }
            }
        }

    }
}
</style>