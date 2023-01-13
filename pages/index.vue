<template>
  <div class="top">
      <div class="intro">
        <TheContainer>
        <div class="title shadow">
          apps / softs
        </div>
        <div class="desc shadow3">
          おすすめのアプリケーション・ソフトウェアを紹介します。
        </div>
        </TheContainer>
      </div>
    <TheContainer>
      <div class="content">
        <AppButton
          :imageUrl="require(`~/assets/Images/logo-app-figma.webp`)"
          title="NaN"
        />
        <AppButton
          :imageUrl="require(`~/assets/Images/logo-app-figma.webp`)"
          desc="yooo"
          title="NaN"
        />
        <AppButton
          :imageUrl="require(`~/assets/Images/logo-app-figma.webp`)"
          desc="yooo"
          title="NaN"
        />
        <AppButton
          :imageUrl="require(`~/assets/Images/logo-app-figma.webp`)"
          desc="yooo"
          title="NaN"
        />
        <AppButton
          :imageUrl="require(`~/assets/Images/logo-app-figma.webp`)"
          desc="yooo"
          title="NaN"
        />
        <AppButton
          :imageUrl="require(`~/assets/Images/logo-app-figma.webp`)"
          desc="yooo"
          title="NaN"
        />

      </div>
    </TheContainer>
  </div>
</template>

<script>
</script>

<style lang='scss' scoped>
.top {
  margin-top: 80px;
}
.intro{
  margin-top:-0.8rem;
  padding-top:2rem;
  padding-bottom: 8rem;
  margin-bottom: 2rem;
  background-color: $accent;
}
.title{
  font-family:$accentfont;
  color:$accent;
  font-size:2rem;
  // width:auto;
  display:inline;
  padding:0.5rem;
  border-radius: 0.5rem;
  background-color:$background;
}
.desc{
  margin-left:1rem;
  margin-top:1rem;
  font-size: 1.5rem;
  color:$background;
  font-weight: bold;
}
.content{
  display:grid;
  grid-template-columns:50% 50%;
  row-gap:1.5rem;
  place-items: center;
  grid-auto-rows: 150px;
  margin-bottom: 2rem;
   @include media-breakpoint-down(md){
    grid-template-columns:100%;
    row-gap:0.5rem;
    grid-auto-rows: 130px;
  }
  }
</style>
