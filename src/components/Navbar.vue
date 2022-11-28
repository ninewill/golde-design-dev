<template>
  <!--header-->
  <header class="nav-down">
    <div class="mainheader">
      <div class="side-left">
        <div class="logo">
          <a
            href="https://www.appedu.com.tw/"
            target="_blank"
            class="home-icon"
            title="金賀獎 golde design award"
            >金賀獎 golde design award</a
          >
        </div>
      </div>
      <div class="side-right">
        <ul class="menu">
          <li><a href="#1">關於金赫獎</a></li>
          <li><a href="#2">5th 頒獎典禮</a></li>
          <li><a href="#3">時線設計展</a></li>
          <li><a href="#4">時線活動</a></li>
        </ul>
        <div class="test-link">
          <a href="#5">測驗</a>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  mounted() {
    $('.menu li a[href^="#"]').click(function () {
      let target = this.hash,
        $target = $(target).offset().top;
      console.log(target, $target);

      $("html, body").animate({ scrollTop: $target }), 1500;
    });
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/mixin.scss";
@import "@/assets/scss/variables.scss";
@import "@/assets/scss/reset.scss";

// * ==========================================================================
// * HEADER 區塊
// * ==========================================================================

header {
  position: fixed;
  z-index: 999;
  top: 0;
  width: 100%;
  //padding: 15px 16px;
  transition: top 0.2s ease-in-out;

  @include min-width(768px) {
    padding: 32px 20px;
  }

  @include min-width(1025px) {
    padding: 32px 60px;
  }

  @include min-width(1440px) {
    //padding: 64px 120px;
    padding-top: 64px;
  }
}

.nav-up {
  top: -154px;
}

.mainheader {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  transition: 0.2s;

  @include min-width(1440px) {
    width: 1200px;
  }

  @include min-width(1920px) {
    width: 1400px;
  }
}

// * ==========================================================================
// *  LOGO
// * ==========================================================================

.logo {
  width: 120px;
  height: 24px;
  display: block;
  margin-left: 5px;
  position: relative;

  @include min-width(768px) {
    width: 150px;
    height: 50px;
  }

  @include min-width(1025px) {
    width: 209px;
    height: 86px;
    margin-left: 0px;
  }

  > a {
    width: 100%;
    height: 100%;
    display: block;
    position: absolute;
    top: 0px;
    left: 0px;
    color: $color-white;
    background: url("@/assets/images/header/gda_normal.svg") no-repeat
      center/contain;
    @include hidetext;
    transition: 0.2s;

    @include min-width(1025px) {
      &:hover {
        background: url("@/assets/images/header/gda_hover.svg") no-repeat
          center/contain;
      }
    }
  }
}

.side-right {
  display: flex;
  align-items: center;

  > ul {
    display: flex;
    align-items: center;

    > li {
      margin-right: 64px;

      &:last-child {
        margin-right: 0;
      }

      > a {
        display: block;
        color: $color-white;
				text-shadow: 0px 0px 12px rgba(0, 0, 0, 0.15);
        transition: 0.2s;

        @include min-width(1025px) {
          &:hover {
            text-shadow: 0px 0px 12px #ffffff;
          }
        }
      }
    }
  }

  .test-link {
    margin-left: 176px;
    background: linear-gradient(
      180deg,
      rgba(255, 255, 255, 0.2) 0%,
      rgba(255, 255, 255, 0) 100%
    );
    border: 1px solid rgba(255, 255, 255, 0.4);
    backdrop-filter: blur(32.5px);

    > a {
      padding: 8px 52px;
      display: block;
      color: $color-white;
    }
  }
}
</style>