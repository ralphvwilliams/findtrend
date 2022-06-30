<template>
  <button>{{ text }}</button>
</template>

<script>
import AppText from './AppText.vue';
export default {
  name: 'AppButtons',
  props: [
    'width',
    'height',
    'bgcolor',
    'radius',
    'text',
    'weight',
    'size',
    'color',
    'style',
  ],
  components: {
    AppText,
  },
};
</script>

<style scoped>
button {
  width: v-bind(width);
  height: v-bind(height);
  background-color: v-bind(bgcolor);
  border-radius: v-bind(radius);
  font-weight: v-bind(weight);
  font-size: v-bind(size);
  color: v-bind(color);
  font-style: v-bind(style);
  border: none;
  font-family: 'Effra';
}
</style>
