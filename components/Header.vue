<template>
  <div class="Header shadow">
    <nuxt-link class="Header__title" to="/">
      apps / softs
    </nuxt-link>
  </div>
</template>

<script>

</script>

<style lang='scss' scoped>
.Header{
  background-color: $background;
  position: fixed;
  top:0;
  left:0;
  width:100%;
  height:70px;
  display:flex;
  align-items: center;
  // border-bottom: 2px solid #616161;
  &__title{
    color:$accent;
    font-size: 2.5rem;
    font-family:'Prosto One', sans-serif;
    text-decoration: none;
    margin-left: 1rem;
    &:hover{
      color:$accent2;
    }
  }
}
</style>
