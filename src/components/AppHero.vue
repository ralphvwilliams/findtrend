<template>
  <header>
    <AppNav></AppNav>
    <section class="hero-container">
      <div class="hero-info">
        <AppText
          class="hero-text"
          height="81px"
          weight="bold"
          size="72px"
          style="normal"
          color="#FFFFFF"
          text="Minimize your trends."
        ></AppText>
        <AppText
          class="hero-text-2"
          height="81px"
          weight="bold"
          size="72px"
          style="normal"
          color="#FFFFFF"
          text="Find the trends!"
        ></AppText>
      </div>
      <div class="smallp">
        <AppText
          class="small-p-1"
          width="666px"
          weight="400"
          size="18px"
          style="normal"
          color="#8B8B8B"
          text="Don't let your computer memory consume all of those browser tabs."
        ></AppText>
        <AppText
          class="small-p-2"
          width="666px"
          weight="400"
          size="18px"
          style="normal"
          color="#8B8B8B"
          text="Findtrend lets you gather all your favorite websites into one place"
        ></AppText>
      </div>
      <div class="hero-button">
        <AppButtons
          width="180px"
          height="57px"
          bgcolor="#A8FF35"
          radius="40px"
          text="Get Started 🔥"
          weight="bold"
          size="18px"
          style="normal"
          color="#000000"
        ></AppButtons>
        <img class="research-img" src="../assets/research.png" />
      </div>
      <div class="hero-cards">
        <div
          class="hero-card"
          v-for="card in cards"
          :id="card.id"
          :key="card.id"
        >
          <img :src="card.imageURL" />
          <AppText
            :text="card.text"
            size="24px"
            weight="lighter"
            color="#FFFFFF"
          ></AppText>
          <img src="../assets/x.png" />
        </div>
      </div>
    </section>
  </header>
</template>

<script>
import AppText from './AppText.vue';
import AppButtons from './AppButtons.vue';
import AppNav from './AppNav.vue';
export default {
  name: 'AppHero',
  components: {
    AppText,
    AppButtons,
    AppNav,
  },
  data() {
    return {
      cards: [
        {
          id: 'first',
          imageURL: require('../assets/twitter.png'),
          text: 'Cryptopunk - Search',
        },
        {
          id: 'second',
          imageURL: require('../assets/pinterest.svg'),
          text: 'Popular Design - Se',
        },
        {
          id: 'third',
          imageURL: require('../assets/facebook.svg'),
          text: 'Product Design - Se',
        },
        {
          id: 'fourth',
          imageURL: require('../assets/basketball.svg'),
          text: 'Elon Musk - Search',
        },
      ],
    };
  },
};
</script>

<style scoped>
header {
  position: relative;
  background-color: black;
  height: 900px;
}

.hero-container {
  text-align: center;
}
.hero-info {
  margin-top: 140px;
}

.smallp {
  margin-top: 24px;
  margin-left: 600px;
}
.hero-button {
  margin-top: 40px;
}

.hero-cards {
  margin-top: 112px;
}

.hero-card {
  display: flex;
  width: 342px;
  height: 82px;
  background: #181818;
  align-items: center;
  gap: 20px;
}

#first {
  position: absolute;
  left: 286px;
  top: 600px;
  transform: rotate(-4deg);
}

#second {
  position: absolute;
  left: 492px;
  top: 670px;
  transform: rotate(2deg);
}

#third {
  position: absolute;
  top: 615px;
  left: 739px;
  transform: rotate(-2deg);
}

#fourth {
  position: absolute;
  top: 665px;
  left: 1008px;
  transform: rotate(4deg);
}

@media only screen and (max-width: 391px) {
  header {
    height: fit-content;
  }
  .hero-text {
    height: auto;
  }
  .hero-text,
  .hero-text-2 {
    font-size: 36px;
  }

  .hero-text-2 {
    margin-top: 0;
  }

  .smallp {
    margin-left: 100px;
  }

  .small-p-1,
  .small-p-2 {
    width: 200px;
  }

  .hero-cards {
    margin-left: 20px;
    padding-bottom: 50px;
  }

  #first,
  #second,
  #third,
  #fourth {
    position: inherit;
  }

  .research-img {
    display: none;
  }
}
</style>
