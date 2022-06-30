<template>
  <AppHero></AppHero>
  <SecondSection></SecondSection>
  <ThirdSection></ThirdSection>
  <FourthSection></FourthSection>
  <FifthSection></FifthSection>
  <SixthSection></SixthSection>
  <Footer></Footer>
</template>

<script>
import AppHero from './components/AppHero.vue';
import SecondSection from './components/SecondSection.vue';
import ThirdSection from './components/ThirdSection.vue';
import FourthSection from './components/FourthSection.vue';
import FifthSection from './components/FifthSection.vue';
import SixthSection from './components/SixthSection.vue';
import Footer from './components/Footer.vue';
export default {
  name: 'App',
  components: {
    AppHero,
    SecondSection,
    ThirdSection,
    FourthSection,
    FifthSection,
    SixthSection,
    Footer,
  },
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
@font-face {
  font-family: 'Effra';
  src: local('Effra'), url(./Fonts/Effra_Std_Rg.ttf) format('truetype');
}
</style>
