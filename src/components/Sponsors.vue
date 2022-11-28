<template>
  <div class="sponsors-wrap">
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
          <span class="subtitle">承辦單位</span>
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
  mounted() {},
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/mixin.scss";
@import "@/assets/scss/variables.scss";

// * ==========================================================================
// * Sponsors 區塊
// * ==========================================================================

.sponsors-wrap {
  width: 80%;
  position: relative;
  display: flex;
  margin: 0 auto;

  &:after {
    content: "";
    width: 480px;
    height: 260px;
    position: absolute;
    top: -220px;
    right: -170px;
    z-index: -1;
    display: block;
    background-image: url("@/assets/images/Visual/point_line_surface/1.png");
  }

  &:before {
		content: "";
    width: 520px;
    height: 410px;
    position: absolute;
    bottom: -300px;
    left: -250px;
    z-index: -1;
    display: block;
    background-image: url("@/assets/images/Visual/point_line_surface/4.png");
  }

  .sponsors-left {
    width: 33.33%;
    padding: 124px 120px;
    background: linear-gradient(
      180deg,
      rgba(255, 255, 255, 0.2) 0%,
      rgba(255, 255, 255, 0.04) 100%
    );
    border: 1px solid rgba(255, 255, 255, 0.3);
    backdrop-filter: blur(32.5px);

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
    width: 66.67%;

    .sponsors-right-t {
      display: flex;
      align-items: center;
      padding: 64px 48px;
      background: linear-gradient(
        180deg,
        rgba(255, 255, 255, 0.2) 0%,
        rgba(255, 255, 255, 0) 100%
      );
      border: 1px solid rgba(255, 255, 255, 0.3);
      backdrop-filter: blur(32.5px);

      .sponsors-list {
        margin-right: 40px;

        &:last-child {
          margin-right: 0;
        }

        .subtitle {
          color: $color-white;
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
        .subtitle {
          color: $color-white;
        }

        > ul {
          padding-left: 0;
          display: flex;
          justify-content: space-between;
          align-items: center;

          > li {
            margin-top: 1rem;

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