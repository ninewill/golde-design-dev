<template>
  <div class="sponsors-wrap">
    <div class="sponsors-wrap-r-b" data-aos="fade-left">
      <img src="@/assets/images/Visual/point_line_surface/1.png" alt="" />
    </div>
    <div class="sponsors-wrap-l-b" data-aos="fade-right">
      <img src="@/assets/images/Visual/point_line_surface/4.png" alt="" />
    </div>
    <div class="sponsors-left">
      <div class="sponsors-main-img">
        <img src="@/assets/images/gda/logo.svg" alt="" />
      </div>
    </div>
    <div class="sponsors-right">
      <div class="sponsors-right-t">
        <div class="sponsors-list">
          <span class="subtitle">主辦單位</span>
          <div class="sponsors-list-img">
            <img src="@/assets/images/company/tw-good-design.svg" alt="" />
          </div>
        </div>
        <div class="sponsors-list">
          <span class="subtitle">承辦單位</span>
          <div class="sponsors-list-img">
            <img src="@/assets/images/company/appedu-Logo.svg" alt="" />
          </div>
        </div>
      </div>
      <div class="sponsors-right-b">
        <div class="sponsors-lis2">
          <span class="subtitle">協辦單位</span>
          <ul>
            <li>
              <img src="@/assets/images/company/ud.svg" alt="" />
            </li>
            <li>
              <img src="@/assets/images/company/wacom.svg" alt="" />
            </li>
            <li>
              <img src="@/assets/images/company/amps.svg" alt="" />
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    AOS.init();
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/mixin.scss";
@import "@/assets/scss/variables.scss";

// * ==========================================================================
// * Sponsors 區塊
// * ==========================================================================

.sponsors-wrap {
  width: 100%;
  position: relative;

  @include min-width(1025px) {
    width: 80%;
    display: flex;
    margin: 0 auto;
  }

  .sponsors-wrap-r-b {
    display: none;

    @include min-width(1025px) {
      width: 480px;
      height: 260px;
      display: block;
      position: absolute;
      top: -220px;
      right: -170px;
      z-index: -1;
    }
  }

  .sponsors-wrap-l-b {
    display: none;

    @include min-width(1025px) {
      width: 520px;
      height: 410px;
      display: block;
      position: absolute;
      bottom: -300px;
      left: -250px;
      z-index: -1;
    }
  }

  .sponsors-left {
    width: 100%;
    padding: 124px 120px;
    background: linear-gradient(
      180deg,
      rgba(255, 255, 255, 0.2) 0%,
      rgba(255, 255, 255, 0.04) 100%
    );
    border: 1px solid rgba(255, 255, 255, 0.3);
    backdrop-filter: blur(32.5px);

    @include min-width(1025px) {
      width: 33.33%;
    }

    .sponsors-main-img {
      width: 70px;
      height: 157px;
      margin: 0 auto;

      > img {
        width: 100%;
      }
    }
  }

  .sponsors-right {
    width: 100%;

    @include min-width(1025px) {
      width: 66.67%;
    }

    .sponsors-right-t {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      padding: 64px 48px;
      background: linear-gradient(
        180deg,
        rgba(255, 255, 255, 0.2) 0%,
        rgba(255, 255, 255, 0) 100%
      );
      border: 1px solid rgba(255, 255, 255, 0.3);
      backdrop-filter: blur(32.5px);

      @include min-width(1025px) {
        flex-direction: row;
        justify-content: start;
      }

      .sponsors-list {
        margin-top: 40px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        @include min-width(1025px) {
          margin-top: 0;
          margin-right: 40px;
          align-items: start;
          justify-content: start;
        }

        &:first-child {
          margin-top: 0;
        }

        &:last-child {
          margin-right: 0;
        }

        .subtitle {
          color: $color-white;
          margin-bottom: 0;

          @include min-width(1025px) {
            margin-bottom: 0rem;
          }
        }

        .sponsors-list-img {
          margin-top: 1rem;

          > img {
            width: 100%;
          }
        }
      }
    }

    .sponsors-right-b {
      padding: 64px 48px;
      background: linear-gradient(
        180deg,
        rgba(255, 255, 255, 0.2) 0%,
        rgba(255, 255, 255, 0) 100%
      );
      border: 1px solid rgba(255, 255, 255, 0.3);
      backdrop-filter: blur(32.5px);

      .sponsors-lis2 {
        display: flex;
        flex-direction: column;
        align-items: center;

        @include min-width(1025px) {
          align-items: start;
        }
        .subtitle {
          color: $color-white;
        }

        > ul {
          padding-left: 0;
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          align-items: center;

          @include min-width(1025px) {
						width: 100%;
            flex-direction: row;
						align-items: stretch;
          }

          > li {
            margin-top: 40px;

						@include min-width(1025px) {
							margin-top: 1rem;
						}

            > img {
              width: 100%;
            }
          }
        }
      }
    }
  }
}
</style>