<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <button v-bind:type="type">
    <slot></slot>
  </button>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Button',
  props: {
    type: String,
    // eslint-disable-next-line vue/require-prop-type-constructor
    default: `button`,
    // eslint-disable-next-line vue/require-prop-type-constructor
    require: true,
  },
};
</script>

<style lang="scss" scoped></style>
