<template>
  <section class="quote">
    <div class="quote__text">
      Digital Assets are the future of private equity
      <div>- Deloitte</div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Quote",
};
</script>

<style lang="scss">
.quote {
  background: #252525;
}
.quote__text {
  padding: 0px auto;
  padding: 50px 0px;
  font-size: 32px;
  font-weight: 600;
  line-height: 44px;
  text-align: center;
  color: #2fcc71;
  @media (max-width: 576px) {
    padding: 28px 15px;
    font-size: 22px;
  }
  & > div {
    font-size: 28px;
    font-weight: 600;
    line-height: 38px;
    text-align: center;
    @media (max-width: 576px) {
      font-size: 20px;
    }
  }
}
</style>
