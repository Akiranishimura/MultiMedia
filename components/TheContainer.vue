
<template>
  <div class="container">
    <slot />
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.container {
  margin: 0 auto;
  width: 1080px;
  padding: 0 $container-padding;
  @include media-breakpoint-down(lg) {
    margin: 0 0;
    max-width: 100%;
  }
}
</style>
