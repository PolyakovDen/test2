<template>
  <div class="about-us__wrapper">
    <div class="about-us__block">
      <v-container fluid class="pa-0">
        <div class="about-us__section d-flex justify-space-between flex-wrap mt-16 pl-5 pr-5">
          <div class="about-us__slider">
            <h2 class="about-us__slider--title">О компании</h2>
            <div class="about-us__slider--wrapper">
              <VueSlickCarousel v-bind="slickOptions">
                <div v-for="(item, i) in items" :key="i" class="about-us__list" >
                  <div class="about-us__item">
                    <p class="about-us__item">{{ item.description }}</p>
                  </div>
                </div>
              </VueSlickCarousel>
            </div>
          </div>
          <div class="about-us">
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
        </div>
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
              breakpoint: 700,
              settings: {
                slidesToShow: 2,
                arrows: true,
              }
            },
            {
              breakpoint: 600,
              settings: {
                slidesToShow: 1,
                arrows: true,
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
            description: 'LOREM LOREM LOREM LOREM'
          },
          {
            description: 'LOREM на LOREM дохода'
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
    background-image: url("/test.png");
    background-position: center center;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: cover;
  }
  .about-us__block {
    display: flex;
    height: 100vh;
  }
  .about-us__slider,
  .about-us {
    width: 600px;
  }
  .about-us__slider--title {
    letter-spacing: 15px;
    text-align: center;
    margin: auto;
    font-size: 62px;
    text-transform: uppercase;
  }
  .about-us__title {
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
    margin-top: 100px;
    position: relative;
  }
  .about-us__list {
    display: flex;
  }
  .about-us__item {
    background-color: #2f6464;
    box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
    width: 140px;
    height: 140px;
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
</style>
