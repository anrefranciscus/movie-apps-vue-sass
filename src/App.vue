<template>
  <div id="app">
    <HeaderComp/>
    <main style="min-height: 100vh">
      <router-view></router-view>
    </main>
  </div>
</template>

<script>
import HeaderComp from "@/components/shared/header/HeaderComp.vue";

export default {
  name: 'App',
  components: {
    HeaderComp
  }
}

</script>
<style lang="scss">
@import "@/assets/style/main.scss";
*,
*:before,
*:after {
  box-sizing: border-box;
}
html,
body {
  margin: 0;
  padding: 0;
  color: #fff;
  font-size: 16px;
  font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif;
  background: $bg;
}
.container {
  width: 100%;
  margin-right: auto;
  margin-left: auto;
  padding: 0 1rem;
}
main {
  display: flex;
  flex-direction: column;
  margin: 0 auto;
}
@media (min-width: 1400px) {
  .container {
    max-width: 1320px;
  }
}
</style>
