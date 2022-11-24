<template>
  <!--main-->
  <div id="main" class="wrap wrap-content">
    <!-- The video -->
    <video autoplay muted loop id="myVideo">
      <source src="@/assets/images/mp4/gold-design.mp4" type="video/mp4" />
    </video>
    <section class="section-block s1">
      <div class="s1-wrap">
        <div class="s1-txt">5TH GOLDEN</div>
        <div class="s1-txt">DESIGN AWARD</div>
        <div class="s1-txt flex">
          DAY-LINE
          <div class="s1-txtt">
            <span>第五屆金赫獎</span>
            <span>年度設計展《時線》</span>
          </div>
        </div>
      </div>
    </section>
    <section class="section-block s2">
      <AboutBlock />
    </section>
    <section class="section-block s3">
			<GdaBlock />
		</section>
    <section class="section-block s4"></section>
    <section class="section-block s5"></section>
    <section class="section-block s6"></section>
    <section class="section-block s7"></section>
    <section class="section-block s8"></section>
  </div>
</template>

<script>
// @ is an alias to /src
import AboutBlock from "@/components/AboutBlock.vue";
import GdaBlock from "@/components/GdaBlock.vue";

export default {
  name: "HomeView",
  components: {
    AboutBlock,
		GdaBlock
  },
};
</script>


<style lang="scss">
@import "@/assets/scss/mixin.scss";
@import "@/assets/scss/variables.scss";
@import "@/assets/scss/reset.scss";
@import "@/assets/scss/main.scss";
@import "@/assets/scss/grid.scss";

.wrap {
  height: 5000px;
}

.section-block {
  width: calc(100% - 40px);
  margin: 0 auto;
  margin-bottom: 20rem;

  @include min-width(768px) {
    width: calc(100% - 80px);
  }

  @include min-width(1024px) {
    width: 935px;
  }

  @include min-width(1440px) {
    width: 1200px;
  }

  @include min-width(1920px) {
    width: 1400px;
  }

  &:first-child {
    margin-top: 0;
  }
}

#myVideo {
  position: fixed;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
  z-index: -1;
}

.s1 {
  .s1-wrap {
    .s1-txt {
      margin-bottom: 3rem;
      color: $color-white;
      line-height: 1;
      letter-spacing: 0.05em;
      font-size: 5.6vw;
      text-shadow: 0px 0px 20px rgba(0, 0, 0, 0.25);
      font-family: "Michroma", sans-serif;

      &:last-child {
        margin-bottom: 0;
      }

      &.flex {
        display: flex;
        align-items: flex-end;

        .s1-txtt {
          margin-bottom: 0.5rem;
          margin-left: 1rem;

          > span {
            margin-top: 1rem;
            display: block;
            color: $color-white;
            font-size: 0.8vw;
          }
        }
      }
    }
  }
}
.s2 {
}
</style>