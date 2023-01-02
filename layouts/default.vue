<template>
  <div>
    <section class="hero is-fullheight is-primary">
      <div class="hero-body slogan">
        <div class="container has-text-centered">
          <p class="title">heal your mind</p>
          <p class="title">shape your <i>future</i>.</p>
        </div>
      </div>

      <div class="hero-foot">
        <nav id="menu" class="navbar header has-shadow is-priamry is-flex" role="navigation"
          aria-label="main navigation">
          <div class="navbar-start">
            <div class="navbar-brand">
              <a class="navbar-item" href="/">
                <logo />
              </a>
            </div>

            <NuxtLink v-for="(item, key) of items" :key="key" :to="item.to" exact-active-class="is-active"
              class="navbar-item is-hidden-touch">
              {{ item.title }}
            </NuxtLink>
          </div>

          <div class="navbar-end is-hidden-touch">
            <div class="navbar-item">
              <div class="buttons">
                <a class="button is-info" href="https://t.me/mentalhealthsupport_bot" target="_blank">
                  <span>try now</span>
                  <b-icon icon="telegram" />
                </a>
              </div>
            </div>
          </div>

          <div class="navbar-burger is-align-self-center" @click="menuExpanded = !menuExpanded">
            <span />
            <span />
            <span />
          </div>
        </nav>
      </div>
    </section>

    <aside v-if="menuExpanded"
      class="column is-3 mobile-menu is-overlay has-background-primary-light is-hidden-desktop">
      <p class="menu-label is-hidden-touch">General</p>
      <ul class="menu-list">
        <li v-for="(item, key) of items" :key="key">
          <NuxtLink :to="item.to" exact-ac0tive-class="is-active">
            <b-icon v-if="item.icon" :icon="item.icon" /> {{ item.title }}
          </NuxtLink>
        </li>
      </ul>
    </aside>

    <section class="main-content">
      <Nuxt />
    </section>

    <footer class="footer">
      <div class="content has-text-centered">
        <p>copyright 2022 by <strong>mexb.ai</strong></p>
      </div>
    </footer>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  name: 'DefaultLayout',
  components: {
    Logo,
  },
  data() {
    return {
      menuExpanded: false,
      items: [
        {
          title: 'our mission',
          icon: 'flag-checkered',
          to: { path: '/', hash: '#mission' },
        },
        {
          title: 'product',
          icon: 'chat',
          to: { path: '/', hash: '#product' },
        },
        {
          title: 'testimonials',
          icon: 'account-multiple-check',
          to: { path: '/', hash: '#testimonials' },
        },
        {
          title: 'team',
          icon: 'human-female-female',
          to: { path: '/', hash: '#team' },
        },
        {
          title: 'contact',
          icon: 'card-account-mail',
          to: { name: 'contact' },
        },
      ],
    }
  },
  head() {
    return {
      title: 'mexb.ai',
      link: [
        {
          rel: 'icon',
          type: 'image/x-icon',
          href: '/favicon.ico',
        },
        {
          rel: 'icon',
          type: 'image/png',
          sizes: '16x16',
          href: '~/assets/favicon/favicon-16x16.png',
        },
        {
          rel: 'icon',
          type: 'image/png',
          sizes: '96x96',
          href: '~/assets/favicon/favicon-96x96.png',
        },
        {
          rel: 'icon',
          type: 'image/png',
          sizes: '32x32',
          href: '~/assets/favicon/favicon-32x32.png',
        },
        {
          rel: 'icon',
          type: 'image/png',
          sizes: '192x192',
          href: '~/assets/favicon/android-icon-192x192.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '180x180',
          href: '~/assets/favicon/apple-icon-180x180.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '152x152',
          href: '~/assets/favicon/apple-icon-152x152.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '144x144',
          href: '~/assets/favicon/apple-icon-144x144.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '152x152',
          href: '~/assets/favicon/apple-icon-152x152.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '144x144',
          href: '~/assets/favicon/apple-icon-144x144.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '120x120',
          href: '~/assets/favicon/apple-icon-120x120.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '114x114',
          href: '~/assets/favicon/apple-icon-114x114.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '76x76',
          href: '~/assets/favicon/apple-icon-76x76.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '72x72',
          href: '~/assets/favicon/apple-icon-72x72.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '60x60',
          href: '~/assets/favicon/apple-icon-60x60.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '57x57',
          href: '~/assets/favicon/apple-icon-57x57.png',
        },
        {
          rel: 'apple-touch-icon',
          type: 'image/png',
          sizes: '120x120',
          href: '~/assets/favicon/apple-icon-120x120.png',
        },
      ],
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'mexb.ai — the future of AI chatbots',
        },
        {
          hid: 'msapplication-TileColor',
          name: 'msapplication-TileColor',
          content: '#e2f4f6',
        },
        {
          hid: 'msapplication-TileImage',
          name: 'msapplication-TileImage',
          content: '/favicon/ms-icon-144x144.png',
        },
        {
          hid: 'theme-color',
          name: 'theme-color',
          content: '#e2f4f6',
        },
        // {
        //   hid: 'og:title',
        //   property: 'og:title',
        //   content: 'mexb.ai',
        // },
        // {
        //   hid: 'og:description',
        //   property: 'og:description',
        //   content: 'mexb.ai — the future of AI chatbots',
        // },
        // {
        //   hid: 'og:image',
        //   property: 'og:image',
        //   content: 'https://mexb.ai/og-image.png',
        // },
        {
          hid: 'og:url',
          property: 'og:url',
          content: 'https://mexb.ai',
        },
        // {
        //   hid: 'twitter:card',
        //   name: 'twitter:card',
        //   content: 'summary_large_image',
        // },
        {
          hid: 'twitter:site',
          name: 'twitter:site',
          content: '@mexbai',
        },
        {
          hid: 'twitter:creator',
          name: 'twitter:creator',
          content: '@mexbai',
        },
        {
          hid: 'twitter:title',
          name: 'twitter:title',
          content: 'mexb.ai',
        },
        {
          hid: 'twitter:description',
          name: 'twitter:description',
          content: 'mexb.ai — the future of AI chatbots',
        },
        // {
        //   hid: 'twitter:image',
        //   name: 'twitter:image',
        //   content: 'https://mexb.ai/og-image.png',
        // }
      ],
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const elems = document.querySelectorAll('.slide-in');
      elems.forEach((element, index) => {
        const isEven = index % 2 === 0;
        const toggleClass = isEven ? 'slide-in-from-left' : 'slide-in-from-right';
        const scrollMin = window.scrollY;
        const scrollMax = scrollMin + window.innerHeight;
        const elemMin = element.offsetTop;
        const elemMax = elemMin + element.offsetHeight;
        if (scrollMax > elemMin && scrollMin < elemMax) {
          element.classList.add(toggleClass);
        } else if (element.classList.contains(toggleClass)) {
          element.classList.remove(toggleClass);
        }
      });
    }
  }
}
</script>

<style>
.slogan {
  background: url('~/assets/imgs/aaron-burden-c4fynAqSQic-unsplash.jpg') no-repeat center center;
  background-size: cover;
  background-attachment: fixed;
}

.navbar-brand {
  font-size: 1.5rem;
}

.footer {
  background-color: unset;
}

.mobile-menu {
  position: absolute;
  top: 4rem;
  z-index: 10;
}

/* Animation */

@keyframes slide-in-from-left {
  from {
    transform: translateX(-100%);
  }

  to {
    transform: translateX(0);
  }
}

@keyframes slide-in-from-right {
  from {
    transform: translateX(+100%);
  }

  to {
    transform: translateX(0);
  }
}

.slide-in {
  animation-duration: 1s;
  animation-fill-mode: both;
}

.slide-in-from-left {
  animation-name: slide-in-from-left;
}

.slide-in-from-right {
  animation-name: slide-in-from-right;
}
</style>
