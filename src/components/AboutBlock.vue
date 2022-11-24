<template>
  <!--header-->
	<div class="about">
		<div class="s2-title">
        <span>ABOUT 金赫獎年度設計競賽</span>
        <h3 class="h3 h3-en">Golden Design Award</h3>
        <h3 class="h3 h3-ch">追尋 實現夢想的軌跡。</h3>
        <span
          >《金赫獎》為「台灣好設計交流協會」＆ 赫綵設計學院
          耗時7年打造的國內設計獎項指標平台，目標推廣台灣設計藝術作品及新生代設計師。藉由《金赫獎》競賽光環以及最嚴謹的評審陣容、制度，為競賽遴選出最具發展潛力的設計藝術作品，更藉此機會為台灣設計創作產業共同努力，發掘新生代的明日之星、將台灣設計軟實力推向更開闊的國際舞台！</span
        >
      </div>
      <div class="s2-w-100">
        <div class="s2-w-50">
          <div class="s2-w-50-img s2-img-l">
            <img src="https://dummyimage.com/372x446/#e9ebee/000" alt="" />
          </div>
        </div>
        <div class="s2-w-50">
          <div class="s2-w-50-img s2-img-r">
            <img src="https://dummyimage.com/470x618/#e9ebee/000" alt="" />
          </div>
          <span>4th 年度最佳設計 - 劉大維 / 放課後的革命</span>
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
// * HEADER 區塊
// * ==========================================================================

.about {
	.s2-title {
    width: 750px;

    > span {
      display: block;
      margin-bottom: 1.5rem;
      line-height: 32px;
      color: $color-white;
    }
    .h3 {
      margin-bottom: 1.5rem;
      color: $color-white;
      font-size: 3.2vw;
      font-family: "Michroma", sans-serif;

      &.h3-ch {
        font-weight: 700;
        font-family: "Noto Serif TC", serif;
      }
    }
  }

  .s2-w-100 {
    margin-top: 158px;
    display: flex;
    justify-content: center;
		align-items: center;

    .s2-w-50 {
      &:first-child {
        margin-right: 105px;
      }

      > span {
        margin-top: 1rem;
        text-align: right;
        display: block;
        color: $color-white;
      }

      .s2-w-50-img {
        &.s2-img-l {
          position: relative;

          &::after {
            content: "";
            width: 226px;
            height: 227px;
            position: absolute;
            bottom: -250px;
            left: -150px;
            z-index: -1;
            display: block;
            background-image: url("@/assets/images/Visual/point_line_surface/5.svg");
          }
        }

        &.s2-img-r {
          position: relative;

          &::after {
            content: "";
            width: 480px;
            height: 260px;
            position: absolute;
            top: -180px;
            right: -200px;
            z-index: -1;
            display: block;
            background-image: url("@/assets/images/Visual/point_line_surface/3.png");
          }
        }
      }
    }
  }
}

</style>