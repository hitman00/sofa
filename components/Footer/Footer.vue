<template>
  <div :class="$style.footer_main">
    <div :class="$style.max_size">
      <div :class="$style.footer_boxs">
        <div :class="$style.title"><span></span>Fundo</div>
        <div :class="$style.copy_right">Fundo, 2021 Allright reserved</div>
      </div>
      <div :class="$style.menobar">
        <div v-for="(i, id) in list" :key="id" :class="$style.meno_box">
          <div :class="$style.menobar_title">{{ i.title }}</div>
          <div
            v-for="(item, p_id) in i.page"
            :key="p_id"
            :class="$style.menobar_page"
          >
            {{ item }}
          </div>
        </div>
      </div>
    </div>
    <div :class="$style.copy_right_2">Fundo, 2021 Allright reserved</div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data: () => ({
    list: [
      {
        title: 'Meno',
        page: ['Home', 'Services', 'Pricing', 'Portofolio'],
      },
      {
        title: 'Contact us',
        page: ['Digimar.co', '(323) 9435', 'Tegal, Indonesia'],
      },
      {
        title: 'Social Media',
        page: ['Digimar.co'],
      },
    ],
  }),
}
</script>

<style lang="scss" module>
.footer_main {
  background: linear-gradient(90deg, #718059 0%, #71815a 49%, #465332 100%);
  color: #fff;
}

.max_size {
  max-width: 1200px;

  margin: 0 auto;
  display: flex;
  padding: 10% 15px 7%;
}

.footer_boxs,
.menobar {
  width: 50%;
  overflow: hidden;
}

.menobar {
  display: flex;
  justify-content: space-between;
}

.title {
  font-weight: 600;
  font-size: 60px;
  display: flex;
  align-items: center;
  span {
    display: block;
    width: 20%;
    padding-bottom: 20%;
    border-radius: 50%;
    background: #bcc9a9;
    margin-left: -11%;
    margin-right: 4%;
  }
}

.copy_right {
  margin-left: 13%;
}
.copy_right_2 {
  display: none;
  text-align: center;
  font-weight: 600;
  padding: 2% 0;
  background: #313416;
}

.meno_box {
  width: 30%;
}

.menobar_title {
  font-size: 18px;
  font-weight: 600;
}

.menobar_page {
  line-height: 3;
  font-weight: 300;
  transition: all 0.3s ease;
  cursor: pointer;
  &:hover {
    opacity: 0.7;
  }
}
@media (max-width: 800px) {
  .max_size {
    flex-direction: column-reverse;
  }

  .footer_boxs {
    margin: 7% auto 0;
    width: 80%;
  }

  .menobar {
    width: 80%;
    margin: 0 auto;
  }

  .copy_right {
    display: none;
  }

  .copy_right_2 {
    display: block;
  }
}

@media (max-width: 600px) {
  .menobar_title {
    font-size: 16px;
  }

  .menobar_page {
    font-size: 14px;
  }
}

@media (max-width: 450px) {
  .menobar_title {
    font-size: 20px;
  }

  .menobar_page {
    font-size: 16px;
  }

  .menobar {
    flex-direction: column;
  }

  .meno_box {
    width: 100%;
    text-align: center;
  }
}
</style>
