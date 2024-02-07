<script>

export default {
  name: "AppHeader",
  data() {
    return {
      ArrayLinksMenu: [
        {
          name: 'Characters',
          link: '#',
          current: false
        },
        {
          name: 'Comics',
          link: '#',
          current: true
        },
        {
          name: 'Movies',
          link: '#',
          current: false
        },
        {
          name: 'TV',
          link: '#',
          current: false
        },
        {
          name: 'Games',
          link: '#',
          current: false
        },
        {
          name: 'Collectibles',
          link: '#',
          current: false
        },
        {
          name: 'Videos',
          link: '#',
          current: false
        },
        {
          name: 'Fans',
          link: '#',
          current: false
        },
        {
          name: 'News',
          link: '#',
          current: false
        },
        {
          name: 'Shop',
          link: '#',
          current: false
        }
      ]
    }
  }
}

</script>

<template>
  <header>
    <figure>
      <img src="../assets/img/dc-logo.png" alt="DC-Logo" width="80">
    </figure>

    <nav>
      <ul>
        <li v-for=" (element, index) in ArrayLinksMenu" :key="index">
          <a :class="element.current ? 'active' : ''" :href="element.link">{{ element.name }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
@use '../style/general' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;

header {

  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 80%;
  margin: 0 auto;
  background-color: white;
  padding-top: 20px;
  padding-bottom: 20px;

  nav {

    ul {

      display: flex;
      gap: 30px;

      li {

        list-style: none;

        a {
          text-decoration: none;
          text-transform: uppercase;
          color: $primary-color;
          font-size: 1rem;
          font-weight: bold;
          padding-bottom: 47px;

          &:hover {
            color: $accent-color;
            border-bottom: 5px solid $accent-color;
          }
        }
      }

    }
  }
}
</style>
