<template>
  <div class="Apps">
    <TheContainer>
      <div class="Apps__Bar">
        <AppBar :imageUrl="require(`~/assets/Images/${imageUrll}`)"
        :title=title
        :desc=copy />
      </div>
      <div class="Apps__box">
        <div class="Apps__content shadow" :style="{
        backgroundImage:`url(${bgUrl})` }">
          <div class="Apps__content__desc shadow2">
            <div class="Apps__content__desc__title"> {{ title }}</div>
            <div class="Apps__content__desc__text" v-html="desc">
            </div>
            <div class="Apps__content__btn shadow" @click="page">
              <span class="txt">ウェブサイトはこちら</span>
            </div>
          </div>
        </div>
      </div>
    </TheContainer>
  </div>
</template>

<script>
export default {
  props: {
    imageUrll: {
      type: String,
      default:"logo-app-figma.webp"
    },
    bgUrl: {
      type: String,
      default:"~/assets/Images/Figma__bg.png"
    },
    href: {
      type: String,
      default:"https://www.figma.com/ja/",
    },
    title: {
      type:String,
      default:"Figma"
    },
    desc: {
      type:String,
      default:"ラウザで動くデザインツール<br /> ブラウザ上でリアルタイムに共同編集が可能<br /> コミュニティによる多彩なプラグインも魅力の一つ<br />最近日本法人が設立され、日本語化も対応している<br />"
    },
    copy: {
      type:String,
      default:"ブラウザで動くデザインツール"
    }

  },
  methods: {
    page() {
      window.location.href = this.href;
    },
  },
};
</script>

<style lang='scss' scoped>
.Apps {
  &__Bar {
    padding-top: 3rem;
  }
  &__box {
    padding: 0 0.5rem 0 0.5rem;
  }
  &__content {
    margin-top: 2.5rem;
    // background-image: url("~/assets/Images/Figma__bg.png");
    background-size: 100%;
    display: flex;
    justify-content: flex-end;
    width: 100%;
    height: auto;
    aspect-ratio: 16/9;
    border-radius: 0.5rem;
    overflow: hidden;
    margin-bottom: 3rem;
    @include media-breakpoint-down(sm) {
      width: 100%;
      aspect-ratio: auto;
      background-size: cover;
      background-position: center;
    }
    &__desc {
      background-color: rgba($background, 0.8);
      padding: 1.5rem 4rem 0 2rem;
      // max-width: 40%;
      &__title {
        font-family: $accentfont;
        font-size: 2rem;
        color: $color;
        margin-bottom: 1rem;
      }
    }
    &__btn {
      margin-top: 1rem;
      position: relative;
      cursor: pointer;
      background-color: $background;
      padding: 0.5rem;
      width: 100%;
      display: flex;
      justify-content: center;
      border-radius: 0.5rem;
      &:hover {
        // background-color: $accent;
        color: $background;
      }
      &:before {
          content: "";
          /*絶対配置で位置を指定*/
          position: absolute;
          top: 0;
          left: 0;
          z-index: 2;
          /*色や形状*/
          background: $accent; /*背景色*/
          width: 100%;
          height: 100%;
          /*アニメーション*/
          transition: transform 0.6s cubic-bezier(0.1, 0, 0.2, 1) 0s;
          transform: scale(0, 1);
          transform-origin: right top;
        }

        /*hoverした際の形状*/
        &:hover:before {
          transform-origin: left top;
          transform: scale(1, 1);
        }
    }
  }
}
.txt{
  z-index: 10;
}

</style>
