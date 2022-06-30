<template>
  <div class="third-text">
    <span class="black"
      >Findtrend helps you increase your productivity and reduce your computer's
      memory load,</span
    >
    <span id="grey">
      an application that can fulfill your daily browsing needs.</span
    >
  </div>
  <div class="card-text">
    <span class="black">FireTrend make +1000 startups grow</span>
  </div>
  <div class="sponsors">
    <div class="sponsor" v-for="image in images" :key="image.id">
      <img :src="image.url" />
    </div>
  </div>
</template>

<script>
import AppText from './AppText.vue';
export default {
  name: 'ThirdSection',
  components: {
    AppText,
  },
  data() {
    return {
      images: [
        {
          id: '1aq',
          url: require('../assets/Microsoft.png'),
        },
        {
          id: '2aq',
          url: require('../assets/Allianz.png'),
        },
        {
          id: '3aq',
          url: require('../assets/UpWork.png'),
        },
        {
          id: '4aq',
          url: require('../assets/Volvo.png'),
        },
        {
          id: '5aq',
          url: require('../assets/grab.png'),
        },
        {
          id: '6aq',
          url: require('../assets/verizon.png'),
        },
        {
          id: '7aq',
          url: require('../assets/coinbase.png'),
        },
        {
          id: '8aq',
          url: require('../assets/Expedia.png'),
        },
        {
          id: '9aq',
          url: require('../assets/Airtable.png'),
        },
        {
          id: '10aq',
          url: require('../assets/Magento.png'),
        },
        {
          id: '11aq',
          url: require('../assets/Carrera.png'),
        },
        {
          id: '12aq',
          url: require('../assets/Bonanaza.png'),
        },
        {
          id: '13aq',
          url: require('../assets/WeTransfer.png'),
        },
        {
          id: '14aq',
          url: require('../assets/suzuki.png'),
        },
        {
          id: '15aq',
          url: require('../assets/algolia.png'),
        },
        {
          id: '16aq',
          url: require('../assets/Heineken.png'),
        },
      ],
    };
  },
};
</script>

<style scoped>
.third-text,
.card-text {
  text-align: center;
  padding-top: 140px;
  margin-left: 140px;
  margin-right: 140px;
}
.black,
#grey {
  font-size: 64px;
  font-weight: 700;
  font-family: 'Effra';
}

#grey {
  color: #adadad;
}

.sponsors {
  margin-top: 80px;
  display: grid;
  grid-template-columns: auto auto auto auto;
  row-gap: 32px;
  column-gap: 32px;
  margin-left: 140px;
  margin-right: 140px;
  margin-bottom: 140px;
}

@media only screen and (max-width: 391px) {
  .third-text,
  .card-text {
    margin-left: 30px;
    margin-right: 30px;
  }
  .black,
  #grey {
    font-size: 36px;
    width: 300px;
    height: 86px;
  }

  .sponsors {
    grid-template-columns: 50px;
    margin-left: 60px;
    margin-right: 30px;
    gap: auto;
    align-items: center;
  }
}
</style>
