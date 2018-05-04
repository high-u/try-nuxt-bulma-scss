<template>
  <nav class="navbar has-background-light">
    <div class="navbar-brand">
      <nuxt-link class="navbar-item" to="/">
        <img src="https://bulma.io/images/bulma-logo.png" alt="Bulma" width="112" height="28">
      </nuxt-link>
      <div class="navbar-burger burger burger-font-icon" @click="showNav = !showNav" :class="{'is-active': showNav}">
        <img src="@/assets/ic_menu_black_24px.svg" />
      </div>
    </div>
    <div id="navbarExampleTransparentExample" class="navbar-menu" :class="{'is-active':showNav}">
      <div class="navbar-start">
        <nuxt-link class="navbar-item" to="/">
          Home
        </nuxt-link>
        <div class="navbar-item has-dropdown is-hoverable">
          <a class="navbar-link" href="/documentation/overview/start/">
            Docs
          </a>
          <div class="navbar-dropdown is-boxed">
            <nuxt-link v-for="item in items" :key="item.title" :to="item.url" class="navbar-item">
              {{ item.title }}
            </nuxt-link>
            <hr class="navbar-divider">
            <a class="navbar-item" href="https://bulma.io/documentation/elements/box/">
              Elements
            </a>
            <a class="navbar-item is-active" href="https://bulma.io/documentation/components/breadcrumb/">
              Components
            </a>
          </div>
        </div>
      </div>
      <div class="navbar-end">
        <div class="navbar-item">
          <div class="field is-grouped">
            <p class="control">
              <a class="bd-tw-button button" data-social-network="Twitter" data-social-action="tweet" data-social-target="http://localhost:4000" target="_blank" href="https://twitter.com/intent/tweet?text=Bulma: a modern CSS framework based on Flexbox&amp;hashtags=bulmaio&amp;url=http://localhost:4000&amp;via=jgthms">
                <span class="icon">
                  <i class="fa fa-twitter"></i>
                </span>
                <span>
                  Tweet
                </span>
              </a>
            </p>
            <p class="control">
              <a class="button is-primary" href="https://github.com/jgthms/bulma/releases/download/0.7.0/bulma-0.7.0.zip">
                <span class="icon">
                  <i class="fa fa-download"></i>
                </span>
                <span>Download</span>
              </a>
            </p>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
import feature from '~/pages/feature.vue'
import contact from '~/pages/contact.vue'

export default {
  components: {
    feature,
    contact
  },
  data: () => ({
    showNav: false,
    items: [
      { title: 'Home', icon: 'home', url: '/' },
      { title: 'Feature', icon: 'code', url: '/feature' },
      { title: 'Contact', icon: 'question_answer', url: '/contact' }
    ]
  })
}
</script>

<style>
.navbar {
  margin-bottom: 20px;
}
.burger-font-icon img {
  height: 30px;
  margin: 10px 0 0 12px;
}
</style>
