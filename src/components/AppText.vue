<template>
  <h3>{{ text }}</h3>
</template>

<script>
export default {
  name: 'AppText',
  props: ['width', 'height', 'weight', 'size', 'color', 'style', 'text'],
};
</script>

<style scoped>
h3 {
  width: v-bind(width);
  height: v-bind(height);
  font-weight: v-bind(weight);
  font-size: v-bind(size);
  color: v-bind(color);
  font-style: v-bind(style);
  font-family: 'Effra';
}
</style>
