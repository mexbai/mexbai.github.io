<template>
  <div class="mexbai-logo">
    <div class="mexb"><span>mexb</span></div>
    <div class="ai"><span>ai</span></div>
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
  display: grid;
  gap: 0;
  grid-template-columns: auto auto;
  line-height: 1.25;
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

div.mexb > span,
div.ai > span {
    position: relative;
    bottom: 0.1em;
  }
</style>
