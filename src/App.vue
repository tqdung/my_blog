<template>
  <div id="app">
    <header-page></header-page>
    <router-view/>
    <footer-page></footer-page>
  </div>
</template>

<script>
import HeaderPage from '@/components/layouts/Header.vue'
import FooterPage from '@/components/layouts/Footer.vue'
export default {
  components: {
    HeaderPage,
    FooterPage
  }
}
</script>
<style lang="scss">
@import '@/assets/scss/common.scss';
#app {
  font-family: 'eb garamond',serif, 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: relative;
  min-height: 100vh;
  position: relative;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
