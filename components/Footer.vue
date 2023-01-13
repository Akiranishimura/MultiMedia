<template>
  <div class="footer">
    <div class="footer__rights shadow3">
    ©2023 Akira Nishimura All rights reserved
    </div>
    <div class="footer__desc shadow3">
      <a href="https://github.com/Akiranishimura" class="Anker">
        github
      </a>
    </div>
  </div>
</template>

<script>

</script>

<style lang='scss' scoped>
.footer{
  width:100%;
  background-color: $accent;
  color:$background;
  display:flex;
  flex-direction: column;
  padding: 2rem 2rem 2rem 6rem;
  // padding-left:4rem;
  &__desc{
    color:$background;
  }
}
.Anker{
  color:$background;

}
</style>
