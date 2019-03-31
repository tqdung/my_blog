<template>
  <footer id="footer">
    <b-container>
      <b-row>
          <b-col sm="8" cols="12">
              <div class="information">
                  <img :src="personal_info.avatar" alt="avatar">
                  <div class="information-content">
                    <h3>{{personal_info.title}}</h3>
                    <p>{{personal_info.descriptions}}</p>
                  </div>
              </div>
          </b-col>
          <b-col sm="4" cols="12">
              <div class="form-subscribe">
                <form>
                  <h4>Join My Mailing List</h4>
                  <input type="text"/>
                  <button>Subscribe Now</button>
                </form>
              </div>
          </b-col>
      </b-row>
      <div class="footer-bottom">
        <b-row>
            <b-col sm="8" cols="12">
              <p>© 2023 by Trần Quốc Dũng. Proudly created with Vue.js</p>
            </b-col>
            <b-col sm="4" cols="12">
                <ul>
                  <li v-for="item in social_links" :key="item.alt">
                    <a :href="item.link" target="_blank">
                      <img :src="item.icon" :alt="item.alt">
                    </a>
                  </li>
                </ul>
            </b-col>
        </b-row>
      </div>
    </b-container>
  </footer>
</template>

<script>
export default {
  name: 'FooterPage',
  data () {
    return {
      personal_info: {
        // avatar: 'https://via.placeholder.com/150x150',
        avatar: require('@/assets/images/avatar/avatar-1.jpg'),
        title: 'About me',
        descriptions: "I'm a web developer, love music and want to make new friends with all people"
      },
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
  }
}
</script>

<style>
</style>
