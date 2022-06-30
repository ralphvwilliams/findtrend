<template>
  <header>
    <div class="fifth-info">
      <h2>Get your best deal</h2>
    </div>
    <div class="monthly">
      <h4>Monthly</h4>
      <img src="../assets/button.png" />
      <h5>Yearly</h5>
      <img class="savearrow" src="../assets/savearrow.png" />
    </div>
    <img class="arrow-mobile" src="../assets/arrowmobile.png" />
    <div class="price-cards">
      <div class="price-card" v-for="card in cards" :key="card.id">
        <img :src="card.url" />
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'FifthSection',
  data() {
    return {
      cards: [
        {
          id: '1ac',
          url: require('../assets/firstCard.png'),
        },
        {
          id: '2ac',
          url: require('../assets/secondCard.png'),
        },
        {
          id: '3ac',
          url: require('../assets/thirdCard.png'),
        },
      ],
    };
  },
};
</script>

<style scoped>
header {
  background-color: black;
  text-align: center;
}

h2 {
  padding-top: 140px;
  font-family: 'Effra';
  font-style: normal;
  font-weight: 700;
  font-size: 64px;
  color: #ffffff;
}

.monthly {
  margin-top: 40px;
  display: flex;
  gap: 24px;
  align-items: center;
  justify-content: center;
}
.arrow-mobile {
  display: none;
}
h4 {
  font-family: 'Inter';
  font-style: normal;
  font-weight: 500;
  font-size: 24px;
  color: #ffffff;
}

h5 {
  color: #f5f5f5;
  opacity: 0.5;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 500;
  font-size: 24px;
}

.price-cards {
  display: flex;
  gap: 40px;
  align-items: center;
  justify-content: center;
  margin-top: 40px;
  padding-bottom: 140px;
}

@media only screen and (max-width: 391px) {
  h2 {
    font-size: 36px;
  }

  .price-cards {
    display: block;
  }

  .price-card {
    margin-top: 24px;
  }

  h4,
  h5 {
    font-size: 18px;
  }

  .savearrow {
    display: none;
  }

  .arrow-mobile {
    display: block;
    margin-left: 250px;
  }
}
</style>
