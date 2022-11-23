<template>
  <!--footer-->
  <footer id="footer">

  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/mixin.scss";
@import "@/assets/scss/variables.scss";
@import "@/assets/scss/reset.scss";

// * ==========================================================================
// * FOOTER 區塊
// * ==========================================================================

#footer {
  width: 100%;
  padding: 18px 20px;

  @include min-width(768px) {
    padding: 18px 20px;
  }

  @include min-width(1025px) {
    padding: 18px 60px;
  }

  @include min-width(1440px) {
    padding: 1.5rem 120px;
  }
}
</style>