<template>
  <div>
    <Popup v-if="popupShow">asdasd </Popup>
    <Header />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';
import Popup from '@/components/Popup';
import store from '@/store';

export default {
  components: {
    Header,
    Footer,
    Popup,
  },
  computed: {
    popupShow() {
      return this.$store.getters['popup/getPopupShow'];
    },
  },
  // methods: {
  //   submitQuestionForm() {
  //     console.log(
  //       `This name: ${this.name}, this email: ${this.email}, this message: ${this.message}`
  //     );
  //     this.$store.commit('popup/togglePopup');
  //   },
  // },
};
</script>

<style>
html {
  font-family: 'Inter', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  margin: 0 auto;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
</style>
