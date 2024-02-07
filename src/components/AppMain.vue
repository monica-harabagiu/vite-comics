<script>

export default {
    name: "AppHeader"
}

</script>

<template>
    <main>
        <div>
            <h2>-- Content goes here --</h2>
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
    padding-block: 50px;

    div {

        width: 80%;
        margin: 0 auto;

        h2 {

            font-size: 2rem;
        }
    }
}
</style>