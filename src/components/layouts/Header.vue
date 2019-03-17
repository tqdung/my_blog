<template>
  <header id="header_top">
    <b-container>
      <b-row>
        <b-col sm="6" cols="12">
          <div class="header-left">
            <ul>
              <li v-for="route in routes" :key="route.name">
                <router-link :to="route.to">{{route.name}}</router-link>
              </li>
            </ul>
          </div>
        </b-col>
        <b-col sm="6" cols="12">
          <div class="header-right">
            <div class="toggle" @click="openMenu = !openMenu">
              <i class="fa fa-bars"></i>
            </div>
            <ul>
              <li v-for="item in social_links" :key="item.alt">
                <a :href="item.link" target="_blank">
                  <img :src="item.icon" :alt="item.alt">
                </a>
              </li>
            </ul>
          </div>
        </b-col>
      </b-row>
    </b-container>
    <mobile-menu v-bind:openMenu="openMenu" @closeMenu="closeMenu"></mobile-menu>
  </header>
</template>

<script>
import MobileMenu from './MobileMenu.vue'
export default {
  name: 'HeaderPage',
  components: {
    MobileMenu
  },
  data () {
    return {
      openMenu: false,
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
      ],
      social_links: [
        {
          icon: require('@/assets/images/icons/facebook.webp'),
          link: 'https://www.facebook.com/tqdungit',
          alt: 'Facebook'
        },
        {
          icon: require('@/assets/images/icons/instagram.webp'),
          link: 'https://www.instagram.com/tqdungit',
          alt: 'Instagram'
        },
        {
          icon: require('@/assets/images/icons/pinterest.webp'),
          // link: 'https://www.facebook.com/tqdungit',
          alt: 'Pinterest'
        },
        {
          icon: require('@/assets/images/icons/twister.webp'),
          // link: 'https://www.facebook.com/tqdungit',
          alt: 'Twister'
        }
      ]
    }
  },
  methods: {
    closeMenu () {
      this.openMenu = false
    }
  }
}
</script>

<style>
</style>
