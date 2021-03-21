<template>
  <section class="products">
    <div class="container">
      <h1 class="products__title">Products</h1>
      <div class="products__content">
        <div class="products__buttons">
          <div class="products__launchpad btn"><a href="#">Launchpad</a></div>
          <p>
            Help launch startups<br />
            & fund private bussinesses
          </p>
          <div class="products__marketplace btn">
            <a href="#"> Marketplace</a>
          </div>
          <p>
            Browse through stocks on sale<br />
            from private investors
          </p>
        </div>
        <img
          class="products__img"
          src="@/image/Products-phone.png"
          alt="Phone"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Products",
};
</script>

<style lang="scss">
.products {
  margin-top: 59px;
  @media (max-width: 768px) {
    margin-top: 39px;
  }
}
.products__title {
  font-size: 45px;
  font-weight: 600;
  line-height: 61px;
  @media (max-width: 768px) {
    font-size: 35px;
  }
}
.products__content {
  display: flex;
  justify-content: space-around;
  @media (max-width: 768px) {
    flex-direction: column;
    align-items: center;
  }
}
.products__buttons {
  margin-top: 156px;
  display: flex;
  flex-direction: column;
  max-width: 350px;
  @media (max-width: 768px) {
    margin-top: 10px;
  }

  & p {
    margin-top: 10px;
    font-size: 22px;
    font-weight: 400;
    line-height: 30px;
    text-align: center;
    margin-bottom: 74px;
    @media (max-width: 768px) {
      margin-bottom: 20px;
      font-size: 18px;
    }
  }
}
.btn {
  padding: 19px 89px 15px;
  background: transparent;
  font-size: 32px;
  font-weight: 600;
  line-height: 44px;
  text-align: center;
  border-radius: 10px;
  cursor: pointer;
  position: relative;

  @media (max-width: 768px) {
    font-size: 25px;
  }
  @media (max-width: 576px) {
    width: 290px;
    padding: 19px 64px 15px;
  }

  &:focus {
    outline: none;
    -webkit-box-shadow: 0px 0px 8px 4px rgba(150, 150, 150, 0.3);
    -moz-box-shadow: 0px 0px 8px 4px rgba(150, 150, 150, 0.3);
    box-shadow: 0px 0px 8px 4px rgba(150, 150, 150, 0.3);
  }
  &:hover:before {
    width: 100%;
    color: white;
  }
  &:before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 78px;
    color: white;
    background: rgba(150, 150, 150, 0.3);
    transition: all 1s ease-in-out;
    z-index: -100;
  }
}
.products__launchpad {
  border: 5px solid #252525;
}
.products__launchpad > a {
  color: #252525;
  text-decoration: none;
}
.products__marketplace {
  border: 5px solid #2ecc71;
}
.products__marketplace > a {
  color: #2ecc71;
  // border: 5px solid #2ecc71;
  text-decoration: none;
}
.products__img {
  width: 100%;
  max-width: 348px;
  height: auto;
}
</style>
