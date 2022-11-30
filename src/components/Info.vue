<template>
  <div class="info">
    <div class="s5-w-100 align-left">
      <div class="info-txt">
        <div class="s5-title">
          <span class="subtitle">展覽資訊</span>
          <h3 class="h3">INFO.</h3>
        </div>

        <div class="s5-title-2">
          <h4 class="h4">免費入場參觀</h4>
          <div class="s5-title-2-img">
            <img
              src="@/assets/images/Visual/point_line_surface/Free.svg"
              alt=""
            />
          </div>
        </div>

        <div class="s5-title-3">
          <div class="s5-title-2-img">
            <img
              src="@/assets/images/Visual/point_line_surface/time.svg"
              alt=""
            />
          </div>
          <h4 class="h4">【 特殊活動時將延長開放時間 】</h4>
        </div>

        <div class="s5-title-4">
          <p>西本願寺樹心會館</p>
          <p>台北市萬華區中華路一段 174-2 號</p>
          <p>捷運西門站 1 號出口步行 3 分鐘</p>
        </div>
      </div>
      <div class="info-img">
        <img src="https://dummyimage.com/688x432/#e9ebee/000" alt="" />
      </div>
    </div>
    <div class="s5-w-100 align-right">
      <div class="info-txt">
        <div class="s5-title">
          <span class="subtitle">展覽資訊</span>
          <h3 class="h3">INFO.</h3>
        </div>

        <div class="s5-title-2">
          <h4 class="h4">免費入場參觀</h4>
          <div class="s5-title-2-img">
            <img
              src="@/assets/images/Visual/point_line_surface/Free.svg"
              alt=""
            />
          </div>
        </div>

        <div class="s5-title-3">
          <div class="s5-title-2-img">
            <img
              src="@/assets/images/Visual/point_line_surface/time.svg"
              alt=""
            />
          </div>
          <h4 class="h4">【 特殊活動時將延長開放時間 】</h4>
        </div>

        <div class="s5-title-4">
          <p>西本願寺樹心會館</p>
          <p>台北市萬華區中華路一段 174-2 號</p>
          <p>捷運西門站 1 號出口步行 3 分鐘</p>
        </div>
      </div>
      <div class="info-img">
        <img src="https://dummyimage.com/688x432/#e9ebee/000" alt="" />
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
// * INFO 區塊
// * ==========================================================================

.info {
  .s5-w-100 {
    margin-bottom: 13.75rem;

    @include min-width(1025px) {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    // 圖片在右
    &.align-left {
      flex-direction: row;
    }

    // 圖片在左
    &.align-right {
      flex-direction: row-reverse;
    }

    .info-txt {
      width: 100%;

      @include min-width(1025px) {
        width: 35%;
      }
      .s5-title {
        > span {
          line-height: 32px;
          color: $color-white;
        }

        .h3 {
          margin-bottom: 1.5rem;
          color: $color-white;
          font-size: 36px;
          font-family: "Michroma", sans-serif;

          @include min-width(1025px) {
            font-size: 3.2vw;
          }
        }
      }

      .s5-title-2 {
        display: flex;
        align-items: center;
        .h4 {
          font-size: 30px;
          color: $color-white;
          margin-bottom: 0;

          @include min-width(1025px) {
            margin-bottom: 8px;
            font-size: 1.7vw;
          }
        }

        .s5-title-2-img {
          margin-left: 1rem;

          > img {
            width: 100%;
          }
        }
      }

      .s5-title-3 {
        margin-top: 2rem;
        .h4 {
          margin-top: 0.8rem;
          font-size: 14px;
          color: $color-white;

          @include min-width(1025px) {
            font-size: 0.7vw;
          }
        }

        .s5-title-2-img {
          width: 60%;

          @include min-width(1025px) {
            width: 50%;
          }

          > img {
            width: 100%;
          }
        }
      }

      .s5-title-4 {
        margin-top: 2.75rem;

        > p {
					margin-bottom: 0.5rem;
          color: $color-white;

          @include min-width(1025px) {
            margin-bottom: 1rem;
          }
        }
      }
    }

    .info-img {
      width: 100%;
			margin-top: 75px;

      @include min-width(1025px) {
        width: auto;
				margin-top: 0;
      }

      > img {
        width: 100%;
      }
    }
  }
}
</style>