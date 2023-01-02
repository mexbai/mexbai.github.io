<template>
  <main class="container">
    <Mission />
    <Product />
    <Testimonials />
    <Team />
  </main>
</template>

<script>
import Mission from './mission.vue';
import Team from './team.vue';
import Product from './product.vue';
import Testimonials from './testimonials.vue';

export default {
  name: 'IndexPage',
  components: {
    Mission,
    Team,
    Product,
    Testimonials,
},
}
</script>
