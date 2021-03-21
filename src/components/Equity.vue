<template>
  <section class="equity">
    <div class="container">
      <div class="equity__content">
        <div class="equity__text">
          <h1 class="title">Private Equity Made Easy</h1>

          <img class="equity__phone" src="@/image/phone2.png" alt="Phone" />
          <div>
            <p class="subtitle">
              Equiteez is on a mission to make private<br />
              equity easily accesible to all in vestors
            </p>
            <button class="equity__button" type="button">
              Singnup For Free
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Equity",
};
</script>

<style lang="scss">
.equity {
  background-color: #2ecc71;
  z-index: -10;
  color: white;
}
$maxWidth: 1920;
@mixin adaptiv($pcSize, $mobSize) {
  $addSize: $pcSize - $mobSize;
  $maxWidth: $maxWidth - 320;
  font-size: calc(
    #{$mobSize + px} + #{$addSize} * ((100vw - 320px) / #{$maxWidth})
  );
}
.equity__content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 215px;
  padding-bottom: 272px;
  @media (max-width: 768px) {
    padding-top: 8px;
    padding-bottom: 37px;
    text-align: center;
    height: 820px;
  }
  @media (max-width: 320px) {
    height: 780px;
  }
}
.equity__text {
  @media (max-width: 768px) {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    margin: 0 auto;
    height: 100%;
  }
}
.equity__phone {
  position: absolute;
  right: 0;
  top: 50%;
  transform: translateY(-30%);
  max-width: 654px;
  width: calc(50%);
  height: auto;
  @media (max-width: 1600px) {
    right: 0%;
  }
  @media (max-width: 768px) {
    transform: translateY(-20%);
    margin: 0 auto;
    width: calc(100%);
    max-width: 570px;
  }
  @media (max-width: 320px) {
    transform: translateY(-15%);
  }
}

.title {
  @include adaptiv(52, 35);
  font-weight: 700;
  line-height: 71px;
  margin-bottom: 28px;
  z-index: 100;
  @media (max-width: 768px) {
    margin-bottom: 0px;
  }
}
.subtitle {
  @include adaptiv(32, 22);
  font-weight: 400;
  line-height: 44px;
  z-index: 100;
  margin-bottom: 39px;
  @media (max-width: 768px) {
    margin-bottom: 16px;
  }
}
.equity__button {
  background: #252525;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.15);
  border-radius: 10px;
  font-weight: 600;
  font-size: 20px;
  line-height: 27px;
  text-align: center;
  color: white;
  border: 2px solid transparent;
  padding: 14px 46px 15px;
  cursor: pointer;
  z-index: 100;
  transition: box-shadow 0.2s ease-in-out;
  &:hover {
    -webkit-box-shadow: 0px 0px 10px 6px rgba(34, 60, 80, 0.5);
    -moz-box-shadow: 0px 0px 10px 6px rgba(34, 60, 80, 0.5);
    box-shadow: 0px 0px 10px 6px rgba(34, 60, 80, 0.5);
  }
  &:focus {
    outline: none;
    border: 2px solid #34a7f6;
  }
}
</style>
