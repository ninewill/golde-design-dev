<template>
  <div class="about">
    <div class="s2-title">
      <span class="subtitle">ABOUT 金赫獎年度設計競賽</span>
      <h3 class="h3 h3-en">Golden Design Award</h3>
      <h3 class="h3 h3-ch">追尋 實現夢想的軌跡。</h3>
      <span
        >《金赫獎》為「台灣好設計交流協會」＆ 赫綵設計學院
        耗時7年打造的國內設計獎項指標平台，目標推廣台灣設計藝術作品及新生代設計師。藉由《金赫獎》競賽光環以及最嚴謹的評審陣容、制度，為競賽遴選出最具發展潛力的設計藝術作品，更藉此機會為台灣設計創作產業共同努力，發掘新生代的明日之星、將台灣設計軟實力推向更開闊的國際舞台！</span
      >
    </div>
    <div class="s2-w-100">
      <div class="s2-w-50 s2-w-50-l">
        <div class="s2-img-l-b" data-aos="fade-down-left">
          <img src="@/assets/images/Visual/point_line_surface/5.svg" alt="" />
        </div>
        <div class="s2-w-50-img s2-img-l">
          <img src="@/assets/images/Visual/visual-img/01.jpg" alt="" />
        </div>
      </div>
      <div class="s2-w-50 s2-w-50-r">
        <div class="s2-img-r-b" data-aos="fade-up">
          <img src="@/assets/images/Visual/point_line_surface/3.png" alt="" />
        </div>
        <div class="s2-w-50-img s2-img-r">
          <img src="@/assets/images/Visual/visual-img/02.jpg" alt="" />
        </div>
        <span>4th 年度最佳設計 - 劉大維 / 放課後的革命</span>
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
// * About 區塊
// * ==========================================================================

.about {
  .s2-title {
    width: 100%;

		@include min-width(1025px) {
			width: 780px;
		}

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

      &.h3-ch {
        font-weight: 700;
        font-family: "Noto Serif TC", serif;
      }
    }
  }

  .s2-w-100 {
    margin-top: 40px;

    @include min-width(1025px) {
			margin-top: 158px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .s2-w-50 {
      position: relative;

      &:first-child {

				@include min-width(1025px) {
					margin-right: 105px;
				}
      }

      > span {
        margin-top: 1rem;
        text-align: right;
        display: block;
        color: $color-white;
				font-size: 12px;

				@include min-width(1025px) {
					font-size: 16px;
				}
      }

      &.s2-w-50-l {
        position: relative;

        .s2-img-l-b {
          display: none;

          @include min-width(1025px) {
            width: 226px;
            height: 227px;
            display: block;
            position: absolute;
            bottom: -250px;
            left: -150px;
            z-index: -1;
          }

          > img {
            width: 100%;
          }
        }
      }

      &.s2-w-50-r {
        position: relative;
        .s2-img-r-b {
          display: none;

          @include min-width(1025px) {
            width: 480px;
            height: 260px;
            display: block;
            position: absolute;
            top: -180px;
            right: -200px;
            z-index: -1;
          }

          > img {
            width: 100%;
          }
        }
      }

      .s2-w-50-img {
        position: relative;

        &.s2-img-l {
          width: 195px;

					@include min-width(1025px) {
						width: 250px;
          }

					@include min-width(1440px) {
						width: 300px;
          }
        }

        &.s2-img-r {
          width: 251px;
          margin-top: 40px;
					margin-right: 0;
					margin-left: auto;

          @include min-width(1025px) {
						width: 306px;
            margin-top: 0;
          }

					@include min-width(1440px) {
						width: 356px;
          }
        }

        > img {
          width: 100%;
        }
      }
    }
  }
}
</style>