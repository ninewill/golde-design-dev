<template>
  <div class="dayline">
    <div class="s4-w-100">
      <div class="s4-w-20">
        <div class="s4-img">
          <img src="@/assets/images/Visual/main-visual.svg" alt="" />
        </div>
      </div>
      <div class="s4-w-50">
				<div class="s4-w-50-b" data-aos="fade-down-left">
					<img src="@/assets/images/Visual/point_line_surface/5.svg" alt="" />
				</div>
        <div class="s4-title">
          <span class="subtitle">時線年度設計展</span>
          <h3 class="h3">EXHIBITION</h3>
        </div>
        <p>
          將每一幀的日常細細刻畫即是你我認知中的「時間」
          時線。不僅僅是一段一段時間線的累積
          在學習亦或是創作的過程中流動、逐步實現心之所向
          每個人擁有著相同長度的1天、24小時、1440分鐘、86400秒
        </p>
        <p>
          赫綵宛如領航員、培育著每一個夢想成真的豐碩結果，而 時間
          是必須付出的多數成本，
          紀錄著最重要的軌跡，始終深信只要跟著軌跡前行，就能看見成功的剎那。
        </p>
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
// * Dayline 區塊
// * ==========================================================================

.dayline {
  .s4-w-100 {
    margin-top: 2rem;
    display: flex;
    align-items: center;
    justify-content: center;

    .s4-w-20 {
      width: 20%;
      margin-right: 155px;

      .s4-img {
        > img {
          width: 100%;
        }
      }
    }

    .s4-w-50 {
      width: 50%;
			position: relative;

			.s4-w-50-b{
        width: 226px;
        height: 227px;
        position: absolute;
        top: -100px;
        right: -180px;
        z-index: -1;
			}

      .s4-title {
        margin-bottom: 56px;

        > span {
          margin-bottom: 1.5rem;
          line-height: 32px;
          color: $color-white;
        }

        .h3 {
          margin-bottom: 1.5rem;
          color: $color-white;
          font-size: 3.2vw;
          font-family: "Michroma", sans-serif;
        }
      }

      > p {
        margin-bottom: 3rem;
        line-height: 32px;
        color: $color-white;

        &:last-child {
          margin-bottom: 0;
        }
      }
    }
  }
}
</style>