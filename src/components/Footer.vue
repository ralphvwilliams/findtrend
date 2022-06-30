<template>
  <footer>
    <div class="footer-info">
      <div class="left-footer">
        <img src="../assets/footer.png" />
        <h4>Findtrend</h4>
      </div>
      <div class="right-footer">
        <ul>
          <li v-for="link in links" :key="link">
            <a href="#">{{ link }}</a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      links: [
        'Privacy Policy',
        'Terms And Conditions',
        'Contact Us',
        'Careers',
      ],
    };
  },
};
</script>

<style scoped>
.footer-info {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 30px;
  padding-left: 100px;
  padding-right: 100px;
  padding-bottom: 30px;
}

.left-footer {
  display: flex;
  gap: 10px;
  align-items: center;
}

h4 {
  font-family: 'Inter';
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
}

.right-footer ul {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
  list-style: none;
}

a {
  text-decoration: none;
  font-family: 'Effra';
  font-style: normal;
  font-weight: lighter;
  font-size: 18px;
  color: #000000;
}

@media only screen and (max-width: 391px) {
  .footer-info {
    display: block;
  }

  .right-footer {
    padding-bottom: 80px;
  }
  .right-footer ul {
    display: block;
    margin-top: 100px;
  }

  .right-footer li {
    margin-top: 40px;
  }
}
</style>
