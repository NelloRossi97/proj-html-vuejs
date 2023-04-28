<template>
  <HeaderComponent/>
  <MainComponent/>
  <FooterComponent/>
  <div ref="scrollTopButton" class="back-home d-flex justify-content-center align-items-center" @click="scrollToTop" :class="scrolled === false ? 'invisible' : ''">
    <a href="">
      <i class="fa-solid fa-arrow-up"></i>
    </a>
  </div>
  <div class="chat d-flex justify-content-center align-items-center">
    <i class="fa-regular fa-comment fs-5"></i>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
  export default {
  name: 'App',
  data() {
    return {
      scrolled : false
    }
  },
  components: { HeaderComponent, MainComponent, FooterComponent },
  methods: {
    scrollToTop() {
      window.scrollTo(0, 0);
      },
    handleScroll() {
        const scrollBtn = this.$refs.scrollTopButton;
        if (window.scrollY > 0) {
          this.scrolled = true;
        } else {
          this.scrolled = false;
        }
      },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  }
  }
</script>

<style lang="scss" scoped>
@use './assets/styles/partials/variables' as *;
.back-home{
  width: 30px;
  height: 30px;
  border-radius: 50%;
  position: fixed;
  right: 80px;
  bottom: 30px;
  border: 1px solid $icons-color;
  background-color: $bg-primary;
  transition: .5s;
  z-index: 900;
  i{
    font-size: .8rem;
  }
  &:hover{
    border: 1px solid $bg-primary;
    background-color: $icons-color;
    cursor: pointer;
    a{
      color: $bg-primary;
    }
  }

  a{
    text-decoration: none;
    color: $icons-color;
  }
}
.chat{
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: rgb(82, 124, 235);
  color: $bg-primary;
  position: fixed;
  right: 20px;
  bottom: 20px;
  transition: .5s;
  z-index: 900;
  &:hover{
    background-color: rgb(74, 116, 227);
    box-shadow: rgba(0, 0, 0, 0.06) 0px 0px 0px 30px inset;
    cursor: pointer;
  }
}
</style>