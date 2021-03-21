<template>
  <section class="securities">
    <div class="container">
      <div class="securities__content">
        <h3 class="securities__title">What Are Digital Securities?</h3>
        <p class="securities__subtitle">
          Digital securities represent traditional assets like equity or
          bonds.<br />
          They carry all of the same legal rights of their paper issued
          counter-parts.
        </p>
        <div class="sprites">
          <div>
            <img class="sprite__img" src="@/image/Sprites1.svg" alt="" />
            <p class="sprite__title">Invest Any Amount</p>
            <p class="sprite__subtitle">
              Start with as little as $1, buy parts of a whole share
            </p>
          </div>
          <div>
            <img class="sprite__img" src="@/image/Sprites2.svg" alt="" />
            <p class="sprite__title">Access Private Equity</p>
            <p class="sprite__subtitle">
              Get access to investments typically reserved for institutions
            </p>
          </div>
          <div>
            <img class="sprite__img" src="@/image/Sprites3.svg" alt="" />
            <p class="sprite__title">Trade 24/7</p>
            <p class="sprite__subtitle">
              Start with as little as $1, buy parts of a whole share
            </p>
          </div>
        </div>
        <form class="securities__feedback">
          <input class="securities__input" type="email" placeholder="E-mail" />
          <button class="securities__button" type="sumbit">
            Get Early Access
          </button>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Securities",
};
</script>

<style lang="scss">
.securities__content {
  margin: 30px 0px;
  @media (max-width: 768px) {
    margin: 16px 0px;
  }
}
.securities__title {
  font-size: 45px;
  font-weight: 600;
  line-height: 61px;
  text-align: center;
  margin-bottom: 30px;
  @media (max-width: 768px) {
    font-size: 35px;
    margin-bottom: 16px;
  }
}
.securities__subtitle {
  font-size: 25px;
  font-weight: 400;
  line-height: 34px;
  text-align: center;
  max-width: 935px;
  margin: 0 auto 50px;

  @media (max-width: 768px) {
    font-size: 18px;
    margin: 0 auto 36px;
  }
}
.sprites {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  @media (max-width: 992px) {
    flex-direction: column;
    align-items: center;
  }
}
.sprite__img {
  display: block;
  margin: 0 auto;
  max-width: 329px;
  width: 100%;
  height: auto;
}
.sprite__title {
  font-size: 30px;
  font-weight: 600;
  line-height: 41px;
  text-align: center;
  margin-top: 30px;
  margin-bottom: 17px;
  @media (max-width: 768px) {
    margin-top: 25px;
    font-size: 22px;
    margin-bottom: 15px;
  }
}
.sprite__subtitle {
  font-size: 22px;
  font-weight: 400;
  line-height: 30px;
  text-align: center;
  margin-bottom: 36px;
  @media (max-width: 768px) {
    font-size: 18px;
    margin-bottom: 31px;
  }
}
.securities__feedback {
  display: flex;
  justify-content: center;
  padding-bottom: 3px;
  @media (max-width: 768px) {
    flex-direction: column;
  }
}
.securities__input {
  padding: 10px 22px 10px 22px;
  width: 445px;
  border: 1px solid #969696;
  border-radius: 10px;
  margin-right: 30px;
  font-size: 20px;
  font-weight: 400;
  line-height: 27px;
  &::placeholder {
    font-size: 20px;
    font-weight: 400;
    line-height: 27px;
    color: #969696;
  }
  @media (max-width: 768px) {
    width: 100%;
    margin-bottom: 15px;
    margin-right: 0px;
    &::placeholder {
      font-size: 18px;
    }
  }
}
.securities__button {
  font-size: 20px;
  font-weight: 600;
  line-height: 27px;
  text-align: center;
  padding: 10px 49px;
  color: white;
  background: #2ecc71;
  border-radius: 10px;
  border: 1px solid transparent;
  cursor: pointer;
  transition: box-shadow 0.2s;
  &:hover {
    box-shadow: 0px 0px 5px 5px rgba($color: #969696, $alpha: 0.3);
  }
  &:focus {
    outline: none;
    border: 1px solid #969696;
  }
}
</style>
