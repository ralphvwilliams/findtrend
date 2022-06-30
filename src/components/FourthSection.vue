<template>
  <header>
    <div class="socials-info">
      <h2>All Platforms connect to FindTrend</h2>
    </div>
    <div class="socials">
      <div class="social" v-for="social in socials" :key="social.id">
        <img :src="social.url" />
      </div>
    </div>
    <div class="socials-mobile">
      <img src="../assets/platform.png" alt="" />
    </div>
    <div class="tweets">
      <div class="tweet" v-for="tweet in tweets" :key="tweet.id">
        <img :src="tweet.url" />
      </div>
    </div>
    <div class="fourth-button">
      <AppButtons
        width="180px"
        height="57px"
        bgcolor="#000000"
        radius="40px"
        text="View More Trends"
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
  name: 'FourthSection',
  data() {
    return {
      socials: [
        {
          id: '1as',
          url: require('../assets/facebookk.png'),
        },
        {
          id: '2as',
          url: require('../assets/Twitterr.png'),
        },
        {
          id: '3as',
          url: require('../assets/baskett.png'),
        },
        {
          id: '4as',
          url: require('../assets/pinetrestt.png'),
        },
        {
          id: '5as',
          url: require('../assets/m.png'),
        },
        {
          id: '6as',
          url: require('../assets/reditt.png'),
        },
        {
          id: '7as',
          url: require('../assets/vk.png'),
        },
        {
          id: '8as',
          url: require('../assets/Linkedinn.png'),
        },
      ],
      tweets: [
        {
          id: '1at',
          url: require('../assets/tweet 1.png'),
        },
        {
          id: '2at',
          url: require('../assets/tweet 2.png'),
        },
        {
          id: '3at',
          url: require('../assets/tweet 3.png'),
        },
      ],
    };
  },
  components: { AppButtons },
};
</script>

<style scoped>
header {
  background-color: #fafafa;
  text-align: center;
}
h2 {
  font-family: 'Effra';
  font-style: normal;
  font-weight: 700;
  font-size: 64px;
  color: black;
  padding-top: 140px;
}
.socials {
  display: grid;
  grid-template-columns: auto auto auto auto auto auto auto auto;
  gap: 24px;
  margin: 80px 140px;
}

.socials-mobile {
  display: none;
}

.tweets {
  margin-top: 40px;
}

.tweet {
  margin-top: 40px;
}

.fourth-button {
  margin-top: 96px;
  padding-bottom: 156px;
}

@media only screen and (max-width: 391px) {
  h2 {
    font-size: 36px;
    margin-left: 18px;
    margin-right: 18px;
  }

  .socials {
    display: none;
  }

  .socials-mobile {
    display: block;
    margin-top: 32px;
  }
  .tweets {
    padding-left: 18px;
    padding-right: 18px;
  }
  .tweet img {
    max-width: 100%;
  }
}
</style>
