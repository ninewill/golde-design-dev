<template>
  <!--header-->
  <header class="nav-down">
    <div class="main-header">
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
        <div class="menu-wrap">
          <ul class="menu">
            <li><a href="#1">關於金赫獎</a></li>
            <li><a href="#2">5th 頒獎典禮</a></li>
            <li><a href="#3">時線設計展</a></li>
            <li><a href="#4">時線活動</a></li>
          </ul>
        </div>
        <div class="menu__toggler"><span></span></div>
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
			$(".menu-wrap").removeClass("active");
			$(".menu__toggler").removeClass("active");
			$(".body").removeClass("hidden");
      $("html, body").animate({ scrollTop: $target }), 1500;
    });

		const body = document.querySelector(".body");
    const toggler = document.querySelector(".menu__toggler");
    const menu = document.querySelector(".menu-wrap");

    toggler.addEventListener("click", () => {
      toggler.classList.toggle("active");
      menu.classList.toggle("active");
			body.classList.toggle("hidden");
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
  padding: 32px 20px;
  transition: top 0.2s ease-in-out;

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

.main-header {
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
  width: 150px;
  height: 50px;
  display: block;
  position: relative;

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
  width: 85%;
  //position: relative;

  @include min-width(1024px) {
    width: auto;
  }
  .menu-wrap {
		padding-top: 135px;
		padding-left: 53px;
		padding-right: 20%;
    position: absolute;
    top: 0px;
    left: 100%;
    z-index: 998;
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: start;
    color: $color-white;
    background: linear-gradient(
      180deg,
      rgba(255, 255, 255, 0.2) 0%,
      rgba(255, 255, 255, 0.14) 100%
    );
    border: 0.526087px solid #ffffff;
    backdrop-filter: blur(17.0978px);
    transition: 300ms left cubic-bezier(0.77, 0, 0.175, 1);

    &.active {
      left: 20%;
    }

    @include min-width(1024px) {
      width: 100%;
			padding-top: 0;
			padding-left: 0;
			padding-right: 0;
      height: auto;
      display: flex;
      align-items: center;
      flex-direction: row;
      position: static;
      background: transparent;
      border: none;
      backdrop-filter: none;
    }

    > ul {
      display: flex;
      align-items: flex-start;
      flex-direction: column;

      @include min-width(1024px) {
				align-items: center;
        flex-direction: row;
      }

      > li {
				margin-bottom: 50px;

        @include min-width(1024px) {
					margin-bottom: 0;
          margin-right: 32px;
        }

        @include min-width(1440px) {
          margin-right: 64px;
        }

        &:last-child {
          margin-right: 0;
        }

        > a {
          display: block;
          color: $color-white;
          text-shadow: 0px 0px 12px rgba(0, 0, 0, 0.15);
					font-size: 30px;
          transition: 0.2s;
					

          @include min-width(1025px) {
						font-size: 16px;

            &:hover {
              text-shadow: 0px 0px 12px #ffffff;
            }
          }
        }
      }
    }
  }

  /*
 * 小於1024 MENU 按鈕
 */
  .menu__toggler {
    position: absolute;
    top: 33px;
    right: 20px;
    height: 48px;
    width: 48px;
    outline: none;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(
      180deg,
      rgba(255, 255, 255, 0.2) 0%,
      rgba(255, 255, 255, 0) 100%
    );
    border: 1px solid rgba(255, 255, 255, 0.4);
    backdrop-filter: blur(32.5px);
    z-index: 999;
    cursor: pointer;

    @include min-width(1024px) {
      display: none;
    }

    span,
    span::before,
    span::after {
      position: absolute;
      content: "";
      width: 28px;
      height: 2.5px;
      background: $color-white;
      border-radius: 20px;
      transition: 500ms cubic-bezier(0.77, 0, 0.175, 1);
    }

    span::before {
      top: -8px;
    }

    span::after {
      top: 8px;
    }

    &.active > span {
      background: transparent;
    }

    &.active > span::before,
    &.active > span::after {
      background: color-white;
      top: 0px;
    }

    &.active > span::before {
      transform: rotate(-225deg);
    }

    &.active > span::after {
      transform: rotate(225deg);
    }
  }
}
</style>