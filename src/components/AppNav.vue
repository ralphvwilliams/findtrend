<template>
  <nav>
    <div class="left-nav">
      <img class="nav-logo" :src="image" />
      <AppText
        class="findtrend"
        weight="bold"
        size="24px"
        style="normal"
        color="#FFFFFF"
        text="Findtrend"
      ></AppText>
    </div>
    <div class="mid-nav" :class="[isClicked ? midNavDisplayed : '', midNav]">
      <AppText
        v-for="item in menuItems"
        class="nav-item"
        weight="400"
        size="18px"
        style="normal"
        color="#FFFFFF"
        :text="item"
      ></AppText>
      <AppText
        class="login-text"
        weight="400"
        size="18px"
        style="normal"
        color="#FFFFFF"
        text="Login"
      ></AppText>
      <AppButtons
        class="register-button"
        width="129px"
        height="42px"
        bgcolor="#FFFFFF"
        radius="40px"
        text="Register"
        weight="400"
        size="18px"
        style="normal"
        color="#000000"
      ></AppButtons>
    </div>
    <div class="right-nav">
      <AppText
        weight="400"
        size="18px"
        style="normal"
        color="#FFFFFF"
        text="Login"
      ></AppText>
      <AppButtons
        width="129px"
        height="30px"
        bgcolor="#FFFFFF"
        radius="40px"
        text="Register"
        weight="400"
        size="18px"
        style="normal"
        color="#000000"
      ></AppButtons>
    </div>
    <div class="burger" @click="burgerClick">
      <img
        class="hamburger"
        :class="[isClicked ? hideBurger : '', hamburgerClass]"
        src="../assets/icon.png"
      />
      <img
        class="close"
        :class="[isClicked ? closeDisplayed : '', closeClass]"
        src="../assets/close.png"
      />
    </div>
  </nav>
</template>

<script>
import AppButtons from './AppButtons.vue';
import AppText from './AppText.vue';
export default {
  name: 'AppNav',
  components: {
    AppButtons,
    AppText,
  },
  data() {
    return {
      image: require('@/assets/NavLogo.png'),
      menuItems: ['About', 'How it works', 'Pricing', 'Solution', 'Features'],
      isClicked: false,
      midNavDisplayed: 'mid-nav-displayed',
      midNav: 'mid-nav',
      hideBurger: 'hide-burger',
      hamburgerClass: 'hamburger',
      closeDisplayed: 'close-displayed',
      closeClass: 'close',
    };
  },

  methods: {
    burgerClick() {
      this.isClicked = !this.isClicked;
    },
  },
};
</script>

<style scoped>
nav {
  background-color: black;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-left: 60px;
  margin-right: 60px;
}

.register-button {
  display: none;
}

.login-text {
  display: none;
}
.mid-nav-displayed {
  display: none;
}
.burger {
  display: none;
}
.left-nav,
.mid-nav,
.right-nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 40px;
}

@media only screen and (max-width: 391px) {
  nav {
    margin-left: 18px;
  }

  .mid-nav {
    display: none;
  }

  .nav-logo {
    padding-top: 32px;
  }
  .mid-nav-displayed {
    display: block;
    position: absolute;
    top: 160px;
    /* left: 160px; */
    background-color: black;
    width: 90%;
  }

  .register-button {
    display: block;
    margin-top: 40px;
    margin-left: 100px;
    margin-bottom: 80px;
  }

  .login-text {
    display: block;
    margin-top: 40px;
    margin-left: 120px;
    margin-bottom: 80px;
  }

  .nav-item {
    margin-top: 40px;
    margin-left: 120px;
  }

  .right-nav {
    display: none;
  }

  .findtrend {
    display: none;
  }

  .burger {
    display: block;
    position: absolute;
    top: 32px;
    right: 18px;
  }

  .close {
    display: none;
  }

  .close-displayed {
    display: block;
    position: absolute;
    right: 10px;
  }

  .hide-burger {
    display: none;
  }
}
</style>
