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
      <a href="#1" class="scroll">
        <svg
          class="c-circle__def-img c-circle__def-img__origin"
          viewBox="0 0 143 143"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <circle
            opacity=".5"
            cx="71.5"
            cy="71.5"
            r="71"
            stroke="#fff"
          ></circle>
        </svg>
        <svg
          class="c-circle__def-img c-circle__def-img__dammy"
          viewBox="0 0 143 143"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <circle opacity="1" cx="71.5" cy="71.5" r="71" stroke="#fff"></circle>
        </svg>
        <span class="c-circle__def-text-cover">
          <span
            class="
              js-hover__text__translateY
              c-circle__def-text
              p-top-philosophy__link-text
            "
          >
            <span
              class="
                js-hover__text__translateY-inside
                p-top-philosophy__link-text-inside
              "
            >
              scroll
            </span>
            <span
              class="
                js-hover__text__translateY-inside__dammy
                p-top-philosophy__link-text-inside__dammy
              "
              aria-hidden="true"
            >
              SCROLL
            </span>
          </span>
        </span>
      </a>
    </section>
    <section id="1" class="section-block s2">
      <AboutBlock />
    </section>
    <section id="2" class="section-block s3">
      <GdaBlock />
    </section>
    <section id="3" class="section-block s4">
      <DayLine />
    </section>
    <section id="4" class="section-block s5">
      <Info />
    </section>
    <section id="5" class="section-block s6">
			<Sponsors />
		</section>
  </div>
</template>

<script>
// @ is an alias to /src
import AboutBlock from "@/components/AboutBlock.vue";
import GdaBlock from "@/components/GdaBlock.vue";
import DayLine from "@/components/DayLine.vue";
import Info from "@/components/Info.vue";
import Sponsors from "@/components/Sponsors.vue";

export default {
  name: "HomeView",
  components: {
    AboutBlock,
    GdaBlock,
    DayLine,
    Info,
		Sponsors,
  },

  mounted() {
    $(".scroll").mouseover(function (e) {
      $(".scroll").removeClass("is-hover-out");
      $(".scroll").addClass("is-hover");
			e.stopPropagation();
    });
    $(".scroll").mouseout(function (e) {
      $(".scroll").removeClass("is-hover");
      $(".scroll").addClass("is-hover-out");
			e.stopPropagation();
    });
		$(".scroll").click(function () {
      let target = this.hash,
        $target = $(target).offset().top;

      $("html, body").animate({ scrollTop: $target }), 1000;
    });
  },
};
</script>


<style lang="scss">
@import "@/assets/scss/mixin.scss";
@import "@/assets/scss/variables.scss";
@import "@/assets/scss/reset.scss";
@import "@/assets/scss/main.scss";
@import "@/assets/scss/grid.scss";
@import "@/assets/scss/animate.scss";

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

	&.s1 {
    margin-bottom: 2rem;
  }

  &.s3 {
    margin-bottom: 9.0625rem;
  }

  &.s4 {
    margin-bottom: 9.0625rem;
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
  position: relative;

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

.subtitle {
  position: relative;
  display: flex;
  align-items: center;
  padding-left: 1rem;

  &:before {
    content: "";
    display: block;
    position: absolute;
    left: 0;
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(32.5px);
  }
}
</style>