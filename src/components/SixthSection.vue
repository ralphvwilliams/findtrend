<template>
  <header>
    <div class="sixth-text">
      <h1>Join us on email for</h1>
      <h2>more trending topics</h2>
    </div>
    <div class="sixth-button">
      <AppButtons
        width="180px"
        height="57px"
        bgcolor="#000000"
        radius="40px"
        text="Join Now"
        weight="bold"
        size="18px"
        style="normal"
        color="#FFFFFF"
      ></AppButtons>
    </div>
  </header>
</template>

<script>
import AppButtons from './AppButtons.vue';
export default {
  name: 'FifthSection',
  components: { AppButtons },
};
</script>

<style scoped>
header {
  background-color: #a8ff35;
  text-align: center;
}

.sixth-text {
  padding-top: 140px;
}

h1 {
  font-family: 'Effra';
  font-style: normal;
  font-weight: 900;
  font-size: 72px;
  color: #000000;
}

h2 {
  font-family: 'Effra';
  font-style: normal;
  font-weight: 900;
  font-size: 72px;
  color: #adadad;
  opacity: 0.5;
}

.sixth-button {
  margin-top: 40px;
  padding-bottom: 140px;
}

@media only screen and (max-width: 391px) {
  h1,
  h2 {
    font-size: 36px;
  }
}
</style>
