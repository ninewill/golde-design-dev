<template>
  <div class="gda">
    <div class="s3-title">
      <span class="subtitle">5th GDA 頒獎典禮</span>
      <h3 class="h3 h3-en">CEREMONY</h3>
    </div>
    <div class="s3-w-100">
      <div class="s3-w-50">
        <div class="s3-w-50-img s3-img-l">
          <img src="https://dummyimage.com/601x524/#e9ebee/000" alt="" />
        </div>
      </div>
      <div class="s3-w-50 s3-w-50-r">
        <div class="s3-w-50-r-b" data-aos="zoom-in">
          <img src="@/assets/images/Visual/point_line_surface/2.png" alt="" />
        </div>
        <div class="s3-w-50-info-wrap">
          <div class="s3-w-50-info">
            <h3 class="h3">赫綵學員設計競賽</h3>
            <p>
              赫綵設計學院為學員所開辦的設計競賽項目，設立八大設計類別：企業形象設計、廣告海報設計、數位繪畫、攝影、網頁及
              UI設計、影視動畫、App
              遊戲、空間設計專案，為鼓勵學員踴躍投稿、挑戰自我設計極限，提供每一類別豐富且優越的獎勵條件。
            </p>
          </div>
          <div class="s3-w-50-info">
            <h3 class="h3">TOPRO盃 - 和平</h3>
            <p>
              自第四屆金赫獎起開辦「To
              Pro盃」，公開徵選傑出設計創作，廣邀台灣各地及赫綵設計學院之國際姐妹校的優秀設計人士共同參與競賽。今年度以「無設限」視覺主軸，象徵設計並無所謂的極限，亦沒有所謂好設計與壞設計之差，並以「和平
              Peace」作為徵件主題，用設計闡述個人對社會議題的觀點。
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="awards">
      <h3 class="h3">本次頒獎典禮 憑邀請信件入場參加</h3>
      <div class="s3-w-100">
        <div class="s3-w-50 blur">
          <span>頒獎典禮 時間</span>
          <h4 class="h4">12.10 (Sat.) 13:00</h4>
        </div>
        <div class="s3-w-50 blur">
          <span>頒獎典禮 地點</span>
          <h4 class="h4 h4-ch">西本願寺樹心會館</h4>
        </div>
      </div>
    </div>
    <div class="map">
      <iframe
        src="https://api.mapbox.com/styles/v1/by19950131/clakpimwp000515s5hhky9goe.html?title=false&access_token=pk.eyJ1IjoiYnkxOTk1MDEzMSIsImEiOiJja2JpeG5jc2QwaHRhMnF0ZGhhMGxjeW41In0.AECZoItrQh71Aj5HmDCU4A&zoomwheel=false#17.85/25.03986/121.507059/-28.8/38"
        title="Monochrome"
        style="border: none"
      ></iframe>
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
// * Gda 區塊
// * ==========================================================================

.gda {
  .s3-title {
    width: 750px;

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

  .s3-w-100 {
    margin-top: 2rem;

    @include min-width(1025px) {
      display: flex;
    }

    .s3-w-50 {
      width: 100%;

      @include min-width(1025px) {
        width: 50%;
      }

      &.blur {
        padding: 24px;
        background: linear-gradient(
          180deg,
          rgba(255, 255, 255, 0.3) 0%,
          rgba(255, 255, 255, 0) 100%
        );
        border: 1px solid rgba(255, 255, 255, 0.3);
        backdrop-filter: blur(32.5px);
      }

      > span {
        margin-top: 1rem;
        text-align: left;
        display: block;
        color: $color-white;
        font-size: 14px;

        @include min-width(1025px) {
          font-size: 0.8vw;
        }
      }

      > .h4 {
        margin-top: 1rem;
        letter-spacing: 0.1em;
        font-size: 26px;
        color: $color-white;
        font-family: "Michroma", sans-serif;

        @include min-width(1025px) {
          font-size: 2.3vw;
        }

        &.h4-ch {
          font-weight: 700;
          font-family: "Noto Serif TC", serif;
        }
      }

      .s3-w-50-img {
        > img {
          width: 100%;
        }
        &.s3-img-l {
          position: relative;
          z-index: 1;
        }
      }

      &.s3-w-50-r {
        position: relative;
        padding: 35.5px;
        background: linear-gradient(
          180deg,
          rgba(255, 255, 255, 0.1) 0%,
          rgba(255, 255, 255, 0.02) 50.4%,
          rgba(255, 255, 255, 0.1) 100%
        );
        backdrop-filter: blur(32.5px);

        .s3-w-50-info-wrap {
          height: 100%;
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          .s3-w-50-info {
            > .h3 {
              padding-bottom: 1rem;
              color: $color-white;
              border-bottom: 1px solid $color-white;
              font-size: 30px;

              @include min-width(1025px) {
                font-size: 2vw;
              }
            }
            > p {
              color: $color-white;
              font-size: 14px;
              line-height: 32px;

              @include min-width(1025px) {
                font-size: 1vw;
              }
            }
          }
        }

        .s3-w-50-r-b {
          display: none;

          @include min-width(1025px) {
            width: 500px;
            height: 432px;
            display: block;
            position: absolute;
            top: -350px;
            left: -250px;
            z-index: -1;
          }

          > img {
            width: 100%;
          }
        }
      }
    }
  }

  .awards {
    margin-top: 125px;

    > .h3 {
      color: $color-white;
      font-size: 18px;
      text-align: center;

      @include min-width(1025px) {
        font-size: 1.3vw;
        text-align: left;
      }
    }
  }

  .map {
    margin-top: 80px;
    padding: 24px;
    background: linear-gradient(
      180deg,
      rgba(255, 255, 255, 0.3) 0%,
      rgba(255, 255, 255, 0) 100%
    );
    border: 1px solid rgba(255, 255, 255, 0.3);
    backdrop-filter: blur(32.5px);

    > iframe {
      width: 100%;
      height: 400px;

      @include min-width(1025px) {
        height: 600px;
      }
    }
  }
}
</style>