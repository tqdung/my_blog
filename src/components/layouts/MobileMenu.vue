<template>
  <div id="mobile-menu" :class="{show: openMenu}">
    <div class="outside" @click="toggle"></div>
    <div class="menu">
      <ul>
        <li v-for="route in routes" :key="route.name">
          <router-link :to="route.to">{{route.name}}</router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: ['openMenu'],
  data () {
    return {
      routes: [
        {
          name: 'Home',
          to: '/'
        },
        {
          name: 'About',
          to: '/about'
        },
        {
          name: 'Travel',
          to: '/travel'
        },
        {
          name: 'Eat',
          to: '/eat'
        },
        {
          name: 'Relax',
          to: '/relax'
        },
        {
          name: 'Videos',
          to: '/videos'
        }
      ]
    }
  },
  methods: {
    toggle () {
      console.log('fafd')
      this.$emit('closeMenu', null)
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/assets/scss/common.scss";
#mobile-menu {
  z-index: $z-index-mobile-menu;
  pointer-events: none;
  //   display: none;
  //   &.show {
  //     display: block;
  //   }
  .menu {
    top: 0;
    left: -80vw;
    width: 80vw;
    height: 100vh;
    background-color: $background-menu;
    position: absolute;
    transition: left 0.3s ease-in-out;

    display: flex;
    align-items: center;
    justify-content: flex-start;

    ul {
      display: flex;
      flex-direction: column;
      padding-left: 25px;
      font-size: 18px;
      font-weight: bold;
      line-height: 36px;
      text-align: left;
    }

    a {
      color: white;
    }
    :focus {
      color: #436ca8;
    }
  }

  .outside {
    width: 100vw;
    height: 100vh;
    left: 0;
    top: 0;
    position: fixed;
    background-color: transparent;
    transition: background-color 0.3s linear;
    z-index: calc($z-index-mobile-menu - 1);
  }
  &.show {
    pointer-events: initial;
    .outside {
      background: #0003;
    }
    .menu {
      left: 0;
    }
  }
}
</style>
