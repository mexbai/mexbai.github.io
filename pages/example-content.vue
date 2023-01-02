<template>
  <section class="section">
    <h2 class="title is-3 has-text-primary">our mission <b-icon icon="rocket" size="is-large" /></h2>
    <h3 class="subtitle is-6 has-text-grey">
      Author: <a href="https://github.com/anteriovieira"> Antério Vieira </a>
    </h3>
    
    <div class="columns is-mobile">
      <card title="Free" icon="github">
        Open source on <a href="https://github.com/buefy/buefy"> GitHub </a>
      </card>

      <card title="Responsive" icon="cellphone-link">
        <b class="has-text-grey"> Every </b> component is responsive
      </card>

      <card title="Modern" icon="alert-decagram">
        Built with <a href="https://vuejs.org/"> Vue.js </a> and
        <a href="http://bulma.io/"> Bulma </a>
      </card>

      <card title="Lightweight" icon="arrange-bring-to-front"> No other internal dependency </card>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MissionPage',
  components: {
    Card,
  },
}
</script>
