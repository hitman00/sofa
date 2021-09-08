<template>
  <div :class="$style.getstart_main">
    <div :class="$style.max_size">
      <div :class="$style.boxs">
        <div :class="$style.title">
          Lets Boost your Business with Digimar Agency
        </div>
        <div :class="$style.description">
          Power up your business with our best digital marketing services.
        </div>
      </div>
      <div :class="$style.boxs">
        <div :class="$style.get_btn">Get Started</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GetStart',
}
</script>

<style lang="scss" module>
.getstart_main {
  color: #fff;
  width: 100%;
  background: linear-gradient(
    90deg,
    rgba(139, 158, 110, 1) 0%,
    rgba(113, 129, 90, 1) 49%,
    rgba(70, 83, 50, 1) 100%
  );
}

.max_size {
  max-width: 1230px;
  margin: 0 auto;
  display: flex;
  padding: 8.6% 0;
}

.boxs {
  width: 50%;
  position: relative;
}

.title {
  font-weight: 600;
  font-size: 45px;
  line-height: 1.2;
}

.description {
  font-weight: 300;
  margin-top: 3%;
}

.get_btn {
  font-weight: 600;
  transition: all 0.3s ease;
  cursor: pointer;
  background: #313416;
  padding: 3% 6.7%;
  display: inline-block;
  position: absolute;
  top: 35%;
  right: 0;
  &:hover {
    opacity: 0.7;
  }
}
</style>
