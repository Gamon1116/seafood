<template>
  <div class="wrapper">
    <div class="md-layout">
        <div class="md-layout-item md-size-40 mx-auto md-small-size-100">
          <md-card>
            <carousel
              :per-page="1"
              loop
              :speed="700"
              autoplay
              :autoplay-timeout="5000"
              :mouse-drag="false"
              navigationEnabled
              navigationNextLabel="<i class='material-icons'>keyboard_arrow_right</i>"
              navigationPrevLabel="<i class='material-icons'>keyboard_arrow_left</i>"
            >
              <slide>
                <!-- 이미지내 text
                <div class="carousel-caption">
                  <h4>
                    <md-icon>location_on</md-icon>
                    Somewhere Beyond, United States
                  </h4>
                </div> -->
                <img :src="carousel1" alt="carousel1" />
              </slide>
              <slide>
                <img :src="carousel2" alt="carousel2" />
              </slide>
              <slide>
                <img :src="carousel3" alt="carousel3" />
              </slide>
            </carousel>
          </md-card>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      carousel1: require("@/assets/img/carousel/carousel1.png"),
      carousel2: require("@/assets/img/carousel/carousel2.png"),
      carousel3: require("@/assets/img/carousel/carousel3.png")
    };
  }
};
</script>

<style lang="scss" scoped>
.vertical-center {
  display: flex;
  align-items: center;
}
.flex-column {
  display: flex;
  flex-direction: column;
}
.md-checkbox,
.md-radio {
  display: flex;
  margin: 0;
  margin-bottom: 0.5rem;
}
</style>
