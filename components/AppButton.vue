<template>
  <div class="AppButton shadow">
    <div class="AppButton__img">
      <figure  class="AppButton__img__content"
      :style="{
        backgroundImage:`url(${imageUrl})` }" />
    </div>
    <div class="AppButton__content">
      <div class="AppButton__content__title">
        {{ title }}
      </div>
      <div class="AppButton__content__desc shadow2">
        {{ desc }}
      </div>
    </div>
  </div>
</template>

<script>
export default{
  props:{
    imageUrl:{
      type:String,
      default:"~/assets/Images/logo-app-figma.webp"
    },
    title:{
      type:String,
      default:"Figma"
    },
    desc:{
      type:String,
      default:"ブラウザ上で動くデザインツール"
    }
  }
}
</script>

<style lang='scss' scoped>
.AppButton{
  width:90%;
  border-radius: 0.5rem;
  height: 120px;
  display:flex;
  overflow: hidden;
  gap:1rem;
  @include media-breakpoint-down(md){
    height:100px;
  }
  cursor: pointer;
  &:hover{
    width:92%;
    height:125px;
    @include media-breakpoint-down(md){
    height:110px;
  }
  }
  &__img{
    height:100%;
    display: flex;
    align-items: center;
    &__content{
      width:160px;
      height:160px;
      background-size: 110%;
    }
  }
  &__content{
    display:flex;
    flex-direction: column;
    &__title{
      font-family: $accentfont;
      color:$accent;
      font-size: 2.5rem;
    }
    &__desc{
      color:$color
    }
  }
}
</style>
