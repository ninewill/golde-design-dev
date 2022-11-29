<template>
  <div id="wrapper" class="layout">
    <Navbar />
    <router-view />
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "HomeView",
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style lang="scss">
@import "@/assets/scss/mixin.scss";
@import "@/assets/scss/variables.scss";
@import "@/assets/scss/reset.scss";
@import "@/assets/scss/main.scss";

html,
body {
  width: 100%;
	//overflow: hidden;
  //height: 100%;
  font-size: map-get($fontsize, 5);
}

body {
  line-height: 1.6em;
  overflow-y: auto;
  overflow-x: hidden;
  position: relative;
  font-size: 1rem;
  font-family: "微軟正黑體", "Microsoft JhengHei", sans-serif, Arial, Helvetica;
  letter-spacing: 0.5px;

	&.hidden{
		overflow: hidden;
	}
}

// * ==========================================================================
// * 包覆整個網頁的區塊
// * ==========================================================================

#wrapper,
#app {
  width: 100%;
  height: 100%;
}

.layout {
  @include min-width(768px) {
  }
}

// * ==========================================================================
// * 主要內容區域（#main 裡面的基本樣式）
// * ==========================================================================

#main {
  padding-bottom: 37px;
  position: relative;

  @include min-width(768px) {
    padding-bottom: 120px;
  }

  @include min-width(1025px) {
    padding-bottom: 185px;
  }
}

// * ==========================================================================
// * 頁面外圍控制整體布局寬度
// * ==========================================================================

.wrap {
  margin: 0 auto;
	padding-top: 17rem;
}

.wrap-content {
	transition: 0.2s;
}
</style>
