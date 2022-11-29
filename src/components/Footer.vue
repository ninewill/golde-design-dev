<template>
  <!--footer-->
  <footer id="footer">
    <div class="main-footer">
      <div class="f-left">
        <div class="f-left-logo">
          <a class="" href="" target="_blank" title="台灣好設計協會">
            台灣好設計協會
          </a>
        </div>
        <p>100 台北市中正區忠孝西路一段6號16樓</p>
        <p>(02)2388-6688 #8006｜平日 9:00-18:30</p>
        <p>appedu@appedu.com.tw</p>
      </div>
      <div class="f-right">
        <p>台灣好設計交流協會、赫綵設計學院保留活動修改活動內容更改之權利，</p>
        <p>最新消息已金赫獎官網官網公告為主</p>
        <p class="copy-right">
          © 2022 Taiwan Good Design Associat. All rights reserved.
        </p>
      </div>
    </div>
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
  padding: 50px 0;
  background: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0.2) 0%,
    rgba(255, 255, 255, 0) 100%
  );
  border-top: 1px solid rgba(255, 255, 255, 0.3);
  backdrop-filter: blur(32.5px);

  @include min-width(768px) {
    padding: 100px 0;
  }

  @include min-width(1025px) {
  }

  @include min-width(1440px) {
  }
}

.main-footer {
  width: calc(100% - 40px);
  margin: 0 auto;

  @include min-width(768px) {
    width: calc(100% - 80px);
  }

  @include min-width(1025px) {
    width: 935px;
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
  }

  @include min-width(1440px) {
    width: 1200px;
  }

  @include min-width(1920px) {
    width: 1400px;
  }

  .f-left {
    .f-left-logo {
      width: 146px;
      height: 30px;
      display: block;
			position: relative;

      > a {
        width: 100%;
        height: 100%;
        display: block;
        position: absolute;
        top: 0px;
        left: 0px;
        color: $color-white;
        background: url("@/assets/images/footer/logo.svg") no-repeat
          center/contain;
        @include hidetext;
        transition: 0.2s;

        @include min-width(1025px) {
          &:hover {
            background: url("@/assets/images/footer/logo_hover.svg") no-repeat
              center/contain;
          }
        }
      }
    }

    > p {
      margin-top: 0.5rem;
      margin-bottom: 0;
      color: $color-white;
      font-size: 14px;
    }
  }

  .f-right {
    > p {
      margin-bottom: 0;
      color: $color-white;
      font-size: 14px;

      &.copy-right {
        opacity: 0.5;
      }
    }
  }
}
</style>