<template>
  <div class="about-us__wrapper" id="about-us">
    <div class="about-us__block">
      <v-container fluid class="pa-0">
        <v-row no-gutters justify-lg="space-between" justify-md="center" justify-sm="center" class="pl-10 pr-10 pb-16" >
          <v-col
            lg="5"
            md="8"
            sm="12">
            <div class="about-us__slider">
              <div data-aos="fade-right" data-aos-duration="1400">
                <h2 class="about-us__slider--title">О компании</h2>
                <div class="about-us__slider--wrapper">
                  <VueSlickCarousel v-bind="slickOptions">
                    <div v-for="(item, i) in items" :key="i" class="about-us__list" >
                      <div class="about-us__item pa-2">
                        <p class="about-us__item--item">{{ item.description }}</p>
                      </div>
                    </div>
                  </VueSlickCarousel>
                </div>
              </div>
            </div>
          </v-col>
          <v-col
            lg="5"
            md="10"
            sm="12">
            <div class="about-us" data-aos="fade-left" data-aos-duration="1400">
              <h3 class="about-us__title">
                <span class="about-us__main--title">New Start</span> - это
              </h3>
              <p class="about-us__description">
                100 + <br>
                <span>проектов</span>
              </p>
              <p class="about-us__description">
                80 + <br>
                <span>клиентов</span>
              </p>
              <p class="about-us__description">
                25 + <br>
                <span>ниш</span>
              </p>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'AboutUs',
    data () {
      return {
        slickOptions: {
          slidesToShow: 3,
          focusOnSelect: true,
          infinite: true,
          autoplay: true,
          autoplaySpeed: 5000,
          speed: 1000,
          arrows: true,
          responsive: [
            {
              breakpoint: 600,
              settings: {
                slidesToShow: 2
              }
            },
            {
              breakpoint: 450,
              settings: {
                slidesToShow: 1
              }
            }
          ]
        },
        items: [
          {
            description: 'Агентство продвижения бизнесов в интернете'
          },
          {
            description: 'Внедряем инновации'
          },
          {
            description: 'Влияем на увеличение дохода'
          },
          {
            description: 'Приводим клиентов для бизнеса'
          },
          {
            description: 'Продвижение в интернете от А до Я'
          },
          {
            description: 'Делаем сайты под ключ'
          },
          {
            description: 'Выводим продажи на новый уровень'
          },
          {
            description: 'Создаем контент, который влюбляет'
          },
        ]
      }
    }
  }
</script>

<style scoped>
  .container {
    width: 1500px;
  }
  .about-us__wrapper {
    background-image: url("/aboutUs-bg.jpg");
    background-repeat:no-repeat;
    -webkit-background-size:cover;
    -moz-background-size:cover;
    -o-background-size:cover;
    background-size:cover;
    background-position:center;
  }
  .about-us__slider--title {
    padding-top: 70px;
    letter-spacing: 15px;
    text-align: center;
    margin: auto;
    font-size: 62px;
    text-transform: uppercase;
  }
  .about-us__title {
    padding-top: 70px;
    font-size: 50px;
    letter-spacing: 10px;
    font-weight: lighter;
  }
  .about-us__main--title {
    font-size: 58px;
    font-weight: bold;
  }
  .about-us__description {
    margin-top: 70px;
    text-align: center;
    font-size: 62px;
    border-bottom: 2px solid;
    line-height: 50px;
  }
  .about-us__description:last-child {
    border-bottom: none;
  }
  .about-us__description span {
    font-size: 30px;
  }
  .about-us__slider--wrapper {
    max-width: 600px !important;
    margin: auto;
    margin-top: 100px;
    position: relative;
  }
  .about-us__list {
    display: flex;
    justify-content: center;
    margin-bottom: 30px;
  }
  .about-us__item {
    background-color: #2f6464;
    box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
    width: 140px;
    height: 140px;
    display: flex;
    justify-content: center;
    align-content: center;
    flex-direction: column;
    text-align: center;
    font-size: 19px;
  }
  ::v-deep .slick-slider {
    overflow: hidden;
  }
  ::v-deep .slick-track {
    display: flex;
    justify-content: space-between;
  }
  ::v-deep .slick-slide {
    padding: 0 30px;
    box-sizing: border-box;
  }

  ::v-deep .slick-arrow {
    position: absolute;
    top: 50%;
    z-index: 10;
    font-size: 0;
    width: 20px;
    height: 50px;
  }

  ::v-deep .slick-prev {
    margin-left: 2px;
    left: -20px;
    top: 50px;
    background: url('/sl-arrow_l.svg') 0 0 / 100% no-repeat;
  }

  ::v-deep .slick-next {
    margin-right: 2px;
    right: -20px;
    top: 50px;
    background: url('/sl-arrow_r.svg') 0 0 / 100% no-repeat;
  }
  @media screen and (max-width: 1264px) {
    .about-us__title {
      text-align: center;
    }
  }
  @media screen and (max-width: 900px) {
    .about-us__slider--title {
      font-size: 55px;
    }
  }
  @media screen and (max-width: 600px) {
    .about-us__slider--title {
      font-size: 45px;
      letter-spacing: 5px;
    }
    .about-us__title {
      font-size: 35px;
    }
    .about-us__main--title {
      font-size: 40px;
    }
    .about-us__description {
      font-size: 46px;
    }
    .about-us__slider--wrapper {
      max-width: 400px !important;
    }
  }
  @media screen and (max-width: 450px) {
    .about-us__slider--wrapper {
      max-width: 200px !important;
    }
  }
  @media screen and (max-width: 340px) {
    .about-us__slider--title {
      word-wrap: break-word;
    }
  }
</style>
