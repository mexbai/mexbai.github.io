<template>
  <div class="column mexbai-logo">
    <div class="mexb">mexb</div>
    <div class="ai">ai</div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Logo',
  props: {
    classNames: {
      type: String,
      required: false,
      default: 'is-primary',
    },
  },
}
</script>

<style scoped>
.mexbai-logo {
  font-family: 'Exo2', sans-serif;
}

.mexb,
.ai {
  border: 0.1em solid;
  height: 1.1em;
  padding: 0 1rem;
  transition: all 150ms linear;
}
</style>
