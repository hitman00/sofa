<template>
  <div :class="$style.slider_main">
    <div :class="$style.slide_text">
      <div :class="$style.title">Why we are best in our Town</div>
      <div :class="$style.description">
        We have 5000+ Review and our customers trust on our Quality product and
        trust own our product. If you order More than $500 we can deliver free
        like Express delivery
      </div>
      <div :class="$style.btn">
        <img src="@/assets/imgs/arrow.png" />
      </div>
    </div>
    <div :class="$style.slide_items">
      <div v-for="(i, id) in list" :key="id" :class="$style.boxs">
        <div :class="$style.slider_image">
          <img :src="i.img" />
        </div>
        <div :class="$style.slider_title">{{ i.title }}</div>
        <div :class="$style.cost">${{ i.cost }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Slider',
  data() {
    return {
      list: [
        {
          img: require('@/assets/imgs/chare1.png'),
          title: 'Green chair with metal',
          cost: '36',
        },
        {
          img: require('@/assets/imgs/kaktos1.png'),
          title: 'Soguaro with Wooden stand',
          cost: '20',
        },
        {
          img: require('@/assets/imgs/flower1.png'),
          title: 'Corn tree wit Wooden rack',
          cost: '10',
        },
      ],
    }
  },
}
</script>

<style lang="scss" module>
.slider_main {
  display: flex;
  margin-top: 5%;
}

.slide_text {
  width: 25%;
}

.title {
  font-size: 40px;
  font-weight: 600;
  line-height: 1.3;
}

.description {
  font-weight: 200;
  margin-top: 15%;
  margin-bottom: 22.7%;
}

.btn {
  width: 55px;
  height: 55px;
  background: #8b9e6e;
  border-radius: 50%;
  margin-left: 10%;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 0.3s ease;
  cursor: pointer;
  img {
    width: 54%;
  }
  &:hover {
    opacity: 0.8;
  }
}

.slide_items {
  width: 75%;
  display: flex;
  justify-content: space-around;
}

.boxs {
  width: 30%;
  transition: all 0.4s ease;
  cursor: pointer;
  &:hover {
    background: #f6f6f6;
  }
}

.slider_image {
  position: relative;
  width: 77%;
  margin: 25.5% auto 0;
  &:before {
    content: '';
    display: block;
    padding-bottom: 147%;
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

.slider_title {
  text-align: center;
  font-weight: 600;
  margin: 18% 26% 11%;
}

.cost {
  font-weight: 600;
  font-size: 20px;
  margin-left: 25%;
  padding-bottom: 20%;
}

@media (max-width: 800px) {
  .slider_main {
    flex-direction: column;
    margin-top: 9%;
  }

  .slide_text,
  .slide_items {
    width: 80%;
    margin: 0 auto;
  }

  .description {
    margin: 6% 0;
  }

  .btn {
    margin: 0 auto 2%;
  }

  .slider_title {
    margin: 18% 3% 11%;
  }

  .cost {
    text-align: center;
    margin-left: 0;
  }
}

@media (max-width: 450px) {
  .title {
    font-size: 30px;
  }

  .slide_items {
    flex-direction: column;
  }

  .boxs {
    width: 80%;
    margin: 0 auto;
  }

  .slider_image {
    width: 51%;
    margin-top: 7.5%;
  }

  .cost {
    padding-bottom: 10%;
  }
}
</style>
