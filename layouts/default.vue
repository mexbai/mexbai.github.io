<template>
  <div>
    <nav
      class="navbar header has-shadow is-primary is-flex"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-start">
        <div class="navbar-brand">
          <a class="navbar-item" href="/">
            <logo />
          </a>
        </div>

        <NuxtLink
          v-for="(item, key) of items"
          :key="key"
          :to="item.to"
          exact-active-class="is-active"
          class="navbar-item is-hidden-touch"
        >
          {{ item.title }}
        </NuxtLink>
      </div>

      <div class="navbar-end is-hidden-touch">
        <div class="navbar-item">
          <div class="buttons">
            <button class="button is-info">
              <span>try now</span>
              <b-icon icon="telegram" />
            </button>
          </div>
        </div>
      </div>

      <div
        class="navbar-burger is-align-self-center"
        @click="menuExpanded = !menuExpanded"
      >
        <span />
        <span />
        <span />
      </div>
    </nav>

    <aside
      v-if="menuExpanded"
      class="column is-3 mobile-menu is-overlay has-background-primary-light is-hidden-desktop"
    >
      <p class="menu-label is-hidden-touch">General</p>
      <ul class="menu-list">
        <li v-for="(item, key) of items" :key="key">
          <NuxtLink :to="item.to" exact-active-class="is-active">
            <b-icon :icon="item.icon" /> {{ item.title }}
          </NuxtLink>
        </li>
      </ul>
    </aside>

    <section class="main-content columns">
      <main class="container column is-10">
        <Nuxt />
      </main>
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
      isMobile: false,
      menuExpanded: false,
      items: [
        {
          title: 'our mission',
          icon: 'home',
          to: { name: 'mission' },
        },
        {
          title: 'team',
          icon: 'lightbulb',
          to: { name: 'team' },
        },
        {
          title: 'contact',
          icon: 'book',
          to: { name: 'contact' },
        },
      ],
    }
  },
}
</script>

<style scoped>
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
</style>
