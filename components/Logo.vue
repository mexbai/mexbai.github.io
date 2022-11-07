<template>
  <div class="columns mexbai-logo">
    <div class="column mexb">mexb</div>
    <div class="column ai">ai</div>
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
  padding: 0.25em;
}

.mexb,
.ai {
  border: 0.1em solid;
  padding: 0 0.25em;
  transition: all 150ms linear;
}

.ai {
  border-left: 0;
  border-color: transparent;
}

.mexbai-logo:hover .mexb {
  border-color: #fff;
  background-color: #fff;
  color: #3b5c61;
}

.mexbai-logo:hover .ai {
  border-color: unset;
}
</style>
