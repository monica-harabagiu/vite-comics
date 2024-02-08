<script>

export default {
    name: "SingleComic",
    props: {
        propsThumb: String,
        propsSeries: String
    }
}

</script>

<template>
    <div class="single-comic">
        <figure>
            <img :src="propsThumb" :alt="propsSeries">
        </figure>
        <h4>{{ propsSeries }}</h4>
    </div>
</template>

<style lang="scss" scoped>
.single-comic {

    flex-basis: calc((100% / 6) - 10px);
    margin-bottom: 30px;

    figure {

        width: 100%;
        margin-bottom: 20px;

        img {
            width: 100%;
            display: block;
            object-fit: cover;
            aspect-ratio: 1;
        }
    }

    h4 {

        text-transform: uppercase;
    }



}
</style>