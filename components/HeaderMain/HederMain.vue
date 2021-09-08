<template>
  <div :class="$style.header_main">
    <div :class="$style.max_size">
      <Header />
      <div :class="$style.sofa_boxs">
        <div :class="$style.boxs">
          <div :class="$style.title">Furniture that everyone Loves</div>
          <div :class="$style.description">
            We have 5000+ Review and our customers trust on our Furniture and
            Quality products.
          </div>
          <div :class="$style.btns">
            <div :class="$style.buy">Buy Now</div>
            <div :class="$style.explore">Explore</div>
          </div>
        </div>
        <div :class="$style.boxs">
          <div :class="$style.frame_image">
            <img src="@/assets/imgs/border2.png" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from './Header/Header.vue'
export default {
  name: 'HeaderMain',
  components: {
    Header,
  },
}
</script>

<style lang="scss" module>
.header_main {
  background: #8b9e6e;
  color: #fff;
}

.max_size {
  max-width: 1230px;
  margin: 0 auto;
}

.sofa_boxs {
  display: flex;
}

.boxs {
  width: 50%;
}

.title {
  font-weight: 600;
  font-size: 64px;
  margin-right: 18%;
  line-height: 1;
}

.description {
  margin: 5% 16% 7% 0;
}

.btns {
  display: flex;
  margin-bottom: 13%;
}

.buy {
  background: #313416;
  padding: 3% 6.7%;
  margin-right: 3%;
}

.explore {
  border: 1px solid #fff;
  padding: 3% 5%;
}

.buy,
.explore {
  font-weight: 600;
  border-radius: 50px;
  transition: all 0.3s ease;
  cursor: pointer;
  &:hover {
    opacity: 0.8;
  }
}

.frame_image {
  position: relative;
  width: 37%;
  top: 10%;
  &:before {
    content: '';
    display: block;
    padding-bottom: 70%;
  }
  img {
    position: absolute;
    width: 100%;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }
}
</style>
