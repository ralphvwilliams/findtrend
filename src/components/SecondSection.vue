<template>
  <header>
    <div class="second-header">
      <AppText
        class="second-info"
        id="secondHeader"
        size="72px"
        color="#000000"
        weight="bold"
        text="Open new tabs is sh*t"
      ></AppText>
    </div>
    <div class="second-img">
      <img src="../assets/ElonLeft.png" />
      <img src="../assets/Elon.png" />
      <img src="../assets/ElonRIght.png" />
    </div>
    <div class="second-text">
      <AppText
        class="second-p"
        size="18px"
        style="normal"
        weight="400"
        color="#000000"
        height="54px"
        text="A solution for your browser tabs and doesn't let your device get slower over time. Get ease and faster to discover a trend with just one tab"
        width="666px"
      ></AppText>
    </div>
  </header>
</template>

<script>
import AppText from './AppText.vue';
export default {
  name: 'SecondSection',
  components: { AppText },
};
</script>

<style scoped>
header {
  background: #a8ff35;
  background-size: cover;
  text-align: center;
}
#secondHeader {
  padding-top: 140px;
}

.second-img {
  padding-top: 60px;
}

.second-text {
  padding-top: 60px;
  padding-bottom: 140px;
  margin-left: 600px;
}

@media only screen and (max-width: 391px) {
  .second-info {
    font-size: 36px;
  }

  .second-img {
    padding-left: 18px;
    padding-right: 18px;
  }
  .second-img img {
    max-width: 100%;
  }

  .second-text {
    margin-left: 100px;
  }

  .second-p {
    width: 200px;
  }
}
</style>
