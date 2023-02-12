<template>
  <header class="header container">
    <div class="header__bar">
      <MenuIcon :active-status="toggleMenu"/>
    </div>
    <nav class="header__nav" :class="{ active: isOpenMenu }">
      <!-- <router-link to="/upcoming" class="header__link">Upcoming</router-link> -->
    </nav>
    <nav class="header__nav" :class="{ active: isOpenMenu }">
      <a href="#" class="header__link">Login</a>
      <a href="#" class="header__link">Register</a>
      <SearchBar/>
    </nav>
  </header>
</template>

<script>

export default {
  name: "HeaderComp",
  components: {
    SearchBar: () =>
      import(
        "@/components/shared/header/SearchBar.vue"
    ),
    MenuIcon: () =>
      import(
      "@/components/shared/header/MenuIcon.vue"
    )
  },
  data() {
    return {
      isOpenMenu: false
    }
  },
  methods: {
    toggleMenu(value) {
      this.isOpenMenu = !value
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/assets/style/__variables.scss";
@import "@/assets/style/__media_query.scss";
.header {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  align-content: stretch;
  align-items: stretch;
  justify-content: flex-start;
  padding: 1rem;
  text-align: center;
  @include mq(tablet) {
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
  &__bar {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    align-content: center;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 1rem;
    @include mq(tablet) {
      margin-bottom: 0;
    }
  }
  &__link {
    padding: 1rem;
    color: #fff;
    text-decoration: none;
    &:hover {
      background: $green;
    }
  }
  &__nav {
    display: none;
    flex-direction: column;
    align-items: stretch;
    justify-content: center;
    @include mq(tablet) {
      display: flex;
      flex-direction: row;
      align-items: center;
    }
  }
}
.active {
  display: flex;
}
</style>
