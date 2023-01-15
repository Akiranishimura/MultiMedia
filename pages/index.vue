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
        <nuxt-link to="/figma" class="link">
          <AppButton
            :imageUrl="require(`~/assets/Images/logo-app-figma.webp`)"
            title="Figma"
          />
        </nuxt-link>
        <nuxt-link to="/Notion" class="link">
        <AppButton
          :imageUrl="require(`~/assets/Images/Notion-logo.png`)"
          desc="多機能メモアプリ"
          title="Notion"
        />
        </nuxt-link>
        <nuxt-link to="/Cron" class="link">
        <AppButton
          :imageUrl="require(`~/assets/Images/Cron-logo.png`)"
          desc="デザイン性に優れたカレンダー"
          title="Cron"
        />
        </nuxt-link>
        <nuxt-link to="goodnotes" class="link">
        <AppButton
          :imageUrl="require(`~/assets/Images/goodnotes-logo.png`)"
          desc="iPad定番ノートアプリ"
          title="GoodNotes5"
        />
        </nuxt-link>
        <nuxt-link to="/Anki" class="link">
        <AppButton
          :imageUrl="require(`~/assets/Images/Anki-logo.png`)"
          title="Anki"
          desc="効率的なフラッシュカード"
        />
        </nuxt-link>
        <nuxt-link to="monkeytype" class="link">
        <AppButton
          :imageUrl="require(`~/assets/Images/Monkeytype-logo.jpg`)"
          title="Monkeytype"
          desc="カスタマイズ可能なタイピングアプリ"
        />
        </nuxt-link>

      </div>
    </TheContainer>
  </div>
</template>

<script>
</script>

<style lang='scss' scoped>

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
  // margin-left:1rem;
  margin-top:1rem;
  font-size: 1rem;
  color:$background;
  // font-weight: bold;
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
.link{
  width:100%;
  text-decoration: none;
  // margin-right:0;
  display:flex;
  justify-content: center;
}
</style>
