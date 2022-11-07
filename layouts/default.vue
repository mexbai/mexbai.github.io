<template>
  <div>
    <nav
      class="navbar header has-shadow is-primary"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <a class="navbar-item" href="/">
          <logo />
        </a>

        <div @click="menuExpanded = !menuExpanded" class="navbar-burger">
          <span />
          <span />
          <span />
        </div>
      </div>
    </nav>

    <aside v-if="menuExpanded" class="column is-3 mobile-menu is-overlay has-background-primary-light">
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
        <p>
          copyright 2022 by <strong>mexb.ai</strong>
        </p>
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
          title: 'Home',
          icon: 'home',
          to: { name: 'index' },
        },
        {
          title: 'Team',
          icon: 'lightbulb',
          to: { name: 'inspire' },
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