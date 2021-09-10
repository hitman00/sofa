<template>
  <div :class="$style.sofa_main">
    <div :class="$style.sofa_image">
      <img src="@/assets/imgs/111.png" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Sofa',
}
</script>

<style lang="scss" module>
.sofa_main {
  display: flex;
  justify-content: end;
}

.sofa_image {
  position: relative;
  width: 64%;
  margin-top: -26%;
  margin-right: 4%;

  &:before {
    display: block;
    content: '';
    padding-bottom: 56%;
  }
  img {
    position: absolute;
    width: 100%;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
  }
}

@media (max-width: 800px) {
  .sofa_image {
    margin: -26% auto 0;
    width: 75%;
  }
}
</style>
