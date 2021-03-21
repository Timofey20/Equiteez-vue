<template>
  <header>
    <div class="container">
      <div class="header">
        <button class="menu" @click="open">
          <img src="@/image/button__menu.svg" alt="" />
        </button>
        <a href="#"> <img src="@/image/Equiteez.svg" alt="Equiteez"/></a>
        <nav class="nav">
          <a class="nav__link" href="#">What Are Digital Securities?</a>
          <a class="nav__link" href="#">Products</a>
          <a class="nav__link" href="#">Digitize Your Business</a>
          <a class="nav__link" href="#">Blog</a>
          <a class="nav__link" href="#">Contact Us</a>
          <div class="nav__under-576">
            <a href="#"
              ><img class="social__link" src="@/image/Twitter.svg" alt="Twitter"
            /></a>
            <a href="#"
              ><img
                class="social__link"
                src="@/image/Facebook.svg"
                alt="Facebook"
            /></a>
            <a href="#"
              ><img
                class="social__link"
                src="@/image/Linkedin.svg"
                alt="Linkedin"
            /></a>
            <a href="#"
              ><img class="social__link" src="@/image/Medium.svg" alt="Medium"
            /></a>
          </div>
        </nav>
        <div class="social">
          <a href="#"
            ><img class="social__link" src="@/image/Twitter.svg" alt="Twitter"
          /></a>
          <a href="#"
            ><img class="social__link" src="@/image/Facebook.svg" alt="Facebook"
          /></a>
          <a href="#"
            ><img class="social__link" src="@/image/Linkedin.svg" alt="Linkedin"
          /></a>
          <a href="#"
            ><img class="social__link" src="@/image/Medium.svg" alt="Medium"
          /></a>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  methods: {
    open: function() {
      let item = document.querySelector(".nav");
      item.classList.toggle("active");
    },
  },
};
</script>

<style lang="scss">
header {
  box-shadow: 0px 1px 10px 0px rgba($color: #000000, $alpha: 0.25);
  position: relative;
}
.container {
  max-width: 1140px;
  margin: 0 auto;
  padding: 0 15px;
}
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 27px 0;
}
.menu {
  display: none;
  border: none;
  background: transparent;
  padding: 0.5rem;
  cursor: pointer;
  @media (max-width: 992px) {
    display: block;
  }
}
.nav {
  padding-left: calc(1.9%);
  display: flex;
  flex-grow: 1;
  justify-content: space-between;
  transition: left 0.5s;
  &__under-576 {
    display: none;
    @media (max-width: 576px) {
      display: flex;
      justify-content: space-evenly;
      margin-bottom: 10px;
    }
  }
  @media (max-width: 992px) {
    position: absolute;
    width: 100%;
    top: 0;
    left: -100%;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    margin-top: 108px;
    background-color: white;
    padding-right: 15px;
    padding-top: 5px;
    z-index: 1000;
    border-radius: 0px 0px 10px 10px;
  }
}
.nav__link {
  font-size: 18px;
  font-weight: 600;
  line-height: 25px;
  color: #000;
  text-decoration: none;
  transition: color 0.2s;
  &:hover {
    color: rgba(0, 0, 0, 0.5);
  }
  @media (max-width: 1200px) {
    font-size: 16px;
    font-weight: 600;
  }
  @media (max-width: 992px) {
    margin-bottom: 20px;
    background-color: #fff;
  }
}
.active {
  left: 0px;
}
.social {
  margin-left: calc(3%);

  display: flex;
  max-width: 141px;
  min-width: 141px;
  justify-content: space-between;
  flex-grow: 1;
  @media (max-width: 576px) {
    display: none;
  }

  &__link {
    transition: transform 0.2s;

    &:hover {
      transform: scale(1.2);
    }
  }
}
</style>
