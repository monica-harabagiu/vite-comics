<script>

export default {
    name: "FooterMain",
    data() {
        return {
            MenuDcComics: [
                {
                    name: 'Characters',
                    link: '#'
                },
                {
                    name: 'Comics',
                    link: '#'
                },
                {
                    name: 'Movies',
                    link: '#'
                },
                {
                    name: 'TV',
                    link: '#'
                },
                {
                    name: 'Games',
                    link: '#'
                },
                {
                    name: 'Videos',
                    link: '#'
                },
                {
                    name: 'News',
                    link: '#'
                }
            ],
            MenuShop: [
                {
                    name: 'Shop DC',
                    link: '#'
                },
                {
                    name: 'Shop DC Collectibles',
                    link: '#'
                }
            ],
            MenuDc: [
                {
                    name: 'Terms Of Use',
                    link: '#'
                },
                {
                    name: 'Privacy policy (New)',
                    link: '#'
                },
                {
                    name: 'Ad Choices',
                    link: '#'
                },
                {
                    name: 'Advertising',
                    link: '#'
                },
                {
                    name: 'Jobs',
                    link: '#'
                },
                {
                    name: 'Subscriptions',
                    link: '#'
                },
                {
                    name: 'Talent Workshops',
                    link: '#'
                },
                {
                    name: 'CPSC Certificates',
                    link: '#'
                },
                {
                    name: 'Ratings',
                    link: '#'
                },
                {
                    name: 'Shop Help',
                    link: '#'
                },
                {
                    name: 'Contact Us',
                    link: '#'
                }
            ],
            MenuSites: [
                {
                    name: 'DC',
                    link: '#'
                },
                {
                    name: 'MAD Magazine',
                    link: '#'
                },
                {
                    name: 'DC Kids',
                    link: '#'
                },
                {
                    name: 'DC Universe',
                    link: '#'
                },
                {
                    name: 'DC Power Visa',
                    link: '#'
                }
            ]
        }
    }
}

</script>

<template>
    <footer>
        <div class="container">

            <div class="menus">

                <div class="col">
                    <div class="single-menu">
                        <h3>DC Comics</h3>
                        <ul>
                            <li v-for="(element, index) in MenuDcComics" :key="index">
                                <a href="element.link">{{ element.name }}</a>
                            </li>
                        </ul>
                    </div>

                    <div class="single-menu">
                        <h3>Shop</h3>
                        <ul>
                            <li v-for="(element, index) in MenuShop" :key="index">
                                <a href="element.link">{{ element.name }}</a>
                            </li>
                        </ul>
                    </div>
                </div>

                <div class="col">
                    <div class="single-menu">
                        <h3>DC</h3>
                        <ul>
                            <li v-for="(element, index) in MenuDc" :key="index">
                                <a href="element.link">{{ element.name }}</a>
                            </li>
                        </ul>
                    </div>
                </div>

                <div class="col">
                    <div class="single-menu">
                        <h3>Sites</h3>
                        <ul>
                            <li v-for="(element, index) in MenuSites" :key="index">
                                <a href="element.link">{{ element.name }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="watermark">
                <figure>
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </figure>
            </div>


        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../style/general' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;

footer {

    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    padding-block: 50px;
    color: white;
    position: relative;
    overflow: hidden;

    .container {
        width: 80%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;

        .menus {

            display: flex;
            gap: 50px;

            .col {
                display: flex;
                flex-direction: column;
                gap: 30px;

                h3 {
                    font-size: 1.5rem;
                    text-transform: uppercase;
                    margin-bottom: 10px;
                }

                li {
                    list-style: none;

                    a {
                        text-decoration: none;
                        color: grey;
                    }
                }
            }
        }

        .watermark {

            position: absolute;
            right: 20%;
            top: 50%;
            transform: translateY(-50%);
        }
    }
}
</style>