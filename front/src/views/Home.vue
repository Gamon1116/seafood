<template>
  <div class="wrapper">
    <parallax
      class="section page-header header-filter"
      :style="headerStyle"
    ></parallax>
    <div class="main main-raised">
      <div class="section home-content">
        <div class="profile-tabs">
          <tabs
            :tab-name="[
              '명진푸드',
              '제품 구입',
              '정기배송',
              '이용후기',
              '오시는길',
            ]"
            :tab-icon="[
              'business',
              'store',
              'local_shipping',
              'preview',
              'location_on',
            ]"
            plain
            nav-pills-icons
            color-button="success"
          >
            <template slot="tab-pane-1">
              <Carousel />
            </template>
            <template slot="tab-pane-2">
              <div class="md-layout">
                <div class="md-layout-item md-size-40 ml-auto">
                  <img :src="tabPane2[0].image" class="rounded" />
                  <img :src="tabPane2[1].image" class="rounded" />
                  <img :src="tabPane2[2].image" class="rounded" />
                </div>
                <div class="md-layout-item md-size-25 mr-auto">
                  <img :src="tabPane1[0].image" class="rounded" />
                  <img :src="tabPane2[3].image" class="rounded" />
                  <img :src="tabPane2[4].image" class="rounded" />
                </div>
              </div>
            </template>
            <template slot="tab-pane-3">
              <div class="md-layout">
                <div class="md-layout-item md-size-25 ml-auto">
                  <img :src="tabPane3[0].image" class="rounded" />
                  <img :src="tabPane3[1].image" class="rounded" />
                </div>
                <div class="md-layout-item md-size-25 mr-auto">
                  <img :src="tabPane3[2].image" class="rounded" />
                  <img :src="tabPane3[3].image" class="rounded" />
                  <img :src="tabPane3[4].image" class="rounded" />
                </div>
              </div>
            </template>
            <template slot="tab-pane-4">
              <div style="text-align:center;">
                이용후기게시판
              </div>
            </template>
            <template slot="tab-pane-5">
              <KakaoMap />
            </template>
          </tabs>
        </div>
      </div>
      <div></div>
    </div>
  </div>
</template>

<script>
import Carousel from "./components/Carouesl";
import { Tabs } from "@/components";
import KakaoMap from "./components/KakaoMap";
export default {
  name: "home",
  components: {
    Tabs,
    Carousel,
    KakaoMap,
  },
  bodyClass: "profile-page",
  data() {
    return {
      tabPane1: [
        { image: require("@/assets/img/examples/studio-1.jpg") },
        { image: require("@/assets/img/examples/studio-2.jpg") },
        { image: require("@/assets/img/examples/studio-4.jpg") },
        { image: require("@/assets/img/examples/studio-5.jpg") },
      ],
      tabPane2: [
        { image: require("@/assets/img/examples/olu-eletu.jpg") },
        { image: require("@/assets/img/examples/clem-onojeghuo.jpg") },
        { image: require("@/assets/img/examples/cynthia-del-rio.jpg") },
        { image: require("@/assets/img/examples/mariya-georgieva.jpg") },
        { image: require("@/assets/img/examples/clem-onojegaw.jpg") },
      ],
      tabPane3: [
        { image: require("@/assets/img/examples/mariya-georgieva.jpg") },
        { image: require("@/assets/img/examples/studio-3.jpg") },
        { image: require("@/assets/img/examples/clem-onojeghuo.jpg") },
        { image: require("@/assets/img/examples/olu-eletu.jpg") },
        { image: require("@/assets/img/examples/studio-1.jpg") },
      ],
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/city-profile.jpg"),
    },
    img: {
      type: String,
      default: require("@/assets/img/faces/christian.jpg"),
    },
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`,
      };
    },
  },
};
</script>

<style lang="scss" scoped>
.section {
  padding: 0;
}

.profile-tabs::v-deep {
  .md-card-tabs .md-list {
    justify-content: center;
  }

  [class*="tab-pane-"] {
    margin-top: 3.213rem;
    padding-bottom: 50px;

    img {
      margin-bottom: 2.142rem;
    }
  }
}
</style>
