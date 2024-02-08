<script>
import SingleComic from './SingleComic.vue';

export default {
    name: "AppHeader",
    components: {
        SingleComic
    },
    data() {
        return {
            comics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    }
}

</script>

<template>
    <main>
        <div class="jumbo">
            <div>
                <h3>Current series</h3>
            </div>
        </div>
        <div class="comics">
            <!-- <h2>-- Content goes here --</h2> -->

            <SingleComic v-for="(element, index) in comics" :key="index" :propsThumb="element.thumb"
                :propsSeries="element.series" />

        </div>
        <div class="more-comics">
            <button>Load more</button>
        </div>

    </main>
</template>

<style lang="scss" scoped>
@use '../style/general' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;


main {
    background-color: $primary-color;
    color: white;
    padding-bottom: 50px;

    .jumbo {

        background-image: url(../assets/img/jumbotron.jpg);
        background-position: top;
        background-size: cover;
        height: 400px;
        margin-bottom: 50px;
        position: relative;

        div {

            position: absolute;
            bottom: -10px;
            left: 10%;
            background-color: $accent-color;
            padding: 10px 20px;

            h3 {

                text-transform: uppercase;
                font-weight: 600;
                font-size: 1.5rem;
            }
        }
    }

    .comics {

        width: 80%;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        gap: 10px;

        h2 {

            font-size: 2rem;
        }

    }

    .more-comics {

        display: flex;
        justify-content: center;
        margin-top: 40px;

        button {
            background-color: $accent-color;
            padding: 10px 30px;
            border: 0;
            color: white;
            text-transform: uppercase;
            font-family: 'PT Sans Narrow', sans-serif;
            font-size: 1.2rem;
            cursor: pointer;
        }
    }
}
</style>