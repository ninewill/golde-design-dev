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
        <img src="@/assets/images/Visual/visual-img/04.jpg" alt="" />
      </div>
    </div>
    <div class="s5-w-100 align-right line">
      <div class="info-txt">
        <div class="s5-title">
          <span class="subtitle">金赫獎年度設計展覽</span>
          <h3 class="h3">12/16 - 27</h3>
        </div>
        <div class="s5-title-2">
          <p>
            第五屆金赫獎年度設計展覽《時線 DAY
            LINE》將盛大展出今年度競賽得獎優秀設計作品，融合「時間線」及「設計創作」的含義嶄新詮釋學習的軌跡。
          </p>
        </div>
        <div class="s5-title-3">
          <ul>
            <li>展出 5th 得獎作品，領略每一件設計背後的創作意涵</li>
            <li>沈浸式互動設計，帶領你穿梭在時間與設計之中交會點</li>
            <li>獨家展出 2022 德國紅點設計獎 Best Of Best 大獎作品</li>
          </ul>
        </div>
      </div>
      <div class="info-img">
        <img src="@/assets/images/Visual/visual-img/05.jpg" alt="" />
      </div>
      <div class="s5-img-l-b" data-aos="fade-down-left">
        <img src="@/assets/images/Visual/point_line_surface/5.svg" alt="" />
      </div>
    </div>
    <div class="s5-w-100 align-left">
      <div class="info-txt">
        <div class="s5-title">
          <span class="subtitle">抽獎活動</span>
          <h3 class="h3">Dream Lottery</h3>
        </div>
        <div class="s5-title-2">
          <p>
            參觀展覽並完成現場指定活動即可免費參加實現「Dream
            Lottery」抽獎活動，就有機會將 Apple iPad、Ｗacom 電繪板、小米
            電子閱讀器 等多項設計師必備的夢幻逸品帶回家！
          </p>
        </div>
        <div class="s5-title-3">
          <ul>
            <li>總價值超過30,000以上多項設計好禮等你帶回家</li>
            <li>
              參加本活動還有機會再獲得「180堂線上設計課程×線下實體設計師講座」雙重學習體驗（價值NT$5,400）
            </li>
          </ul>
        </div>
      </div>
      <div class="info-img">
        <img src="@/assets/images/Visual/visual-img/06.jpg" alt="" />
      </div>
    </div>
    <div class="s5-w-100 align-right">
      <div class="info-txt">
        <div class="s5-title">
          <span class="subtitle">聖誕週文創市集</span>
          <h3 class="h3">12/24</h3>
        </div>
        <div class="s5-title-2">
          <p>
            《時線 DAY
            LINE》聖誕週文創市集，集結來自不同領域的職人、創作者、斜槓青年，琳瑯滿目的文青雜貨、文創商品、聖誕點心，想要探索新的生活靈感，感受滿滿的聖誕氛圍，來逛12/24
            的市集就對了！
          </p>
        </div>
        <div class="s5-title-3">
          <ul>
            <li>市集時間：12/24 (Sat.) 13:00 - 20:00</li>
            <li>市集地點：西本願寺樹心會館 戶外場域</li>
            <li>活動內容：文創市集、手作體驗、闖關遊戲、戶外演出</li>
          </ul>
        </div>
      </div>
      <div class="info-img">
        <img src="@/assets/images/Visual/visual-img/07.jpg" alt="" />
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
    margin-bottom: 5rem;
    display: flex;

    @include min-width(1025px) {
      margin-bottom: 13.75rem;
      justify-content: space-between;
      align-items: center;
    }

    .info-txt {
      width: 100%;
			margin-top: 1rem;
      padding-left: 1.5rem;
      border-left: 2px solid rgba(255, 255, 255, 0.3);
      order: 2;

      @include min-width(1025px) {
        width: 35%;
				margin-top: 0;
				padding-left: 3rem;
        order: 1;
      }
      .s5-title {
        > span {
          line-height: 32px;
          color: $color-white;
        }

        .h3 {
          margin-bottom: 1.5rem;
          color: $color-white;
          font-size: 32px;
          font-family: "Michroma", sans-serif;

          @include min-width(1025px) {
            font-size: 3vw;
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
            font-size: 32px;
          }

          @include min-width(1280px) {
            font-size: 1.7vw;
          }
        }

        .s5-title-2-img {
          margin-left: 1rem;

          > img {
            width: 100%;
          }
        }

        > p {
          line-height: 32px;
          color: $color-white;
        }
      }

      .s5-title-3 {
        margin-top: 2rem;

        > ul {
          padding-left: 0;
          list-style-type: disc;

          > li {
            margin-bottom: 1rem;
            color: $color-white;

            &:last-child {
              margin-bottom: 0;
            }
          }
        }
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

    // 圖片在右
    &.align-left {
      flex-direction: column;

      @include min-width(1025px) {
        flex-direction: row;
      }
    }

    // 圖片在左
    &.align-right {
      flex-direction: column;

      @include min-width(1025px) {
        flex-direction: row-reverse;
      }
    }

    &.line {
      position: relative;

      .s5-img-l-b {
        display: none;

        @include min-width(1025px) {
          width: 226px;
          height: 227px;
          display: block;
          position: absolute;
          bottom: -150px;
          left: -50px;
          z-index: 1;
        }

        > img {
          width: 100%;
        }
      }
    }

    .info-img {
      width: 100%;
      order: 1;

      @include min-width(1025px) {
        width: 60%;
        height: 100%;
        margin-top: 0;
        order: 2;
      }

      > img {
        width: 100%;
        height: 100%;
      }
    }
  }
}
</style>