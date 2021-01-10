<template>
  <div class="" id="cases">
    <div class="cases__block">
      <div class="cases__block--wrapper">
        <h2 class="cases__title" data-aos="flip-up">
          Успешные кейсы
        </h2>
      </div>
    </div>
    <div class="cases__wrapper">
      <VueSlickCarousel v-bind="slickOptions">
        <div data-aos="fade-left" v-for="(item, i) in items" :key="i" class="cases__item--list">
          <div class="cases__item--item">
            <div class="cases__item--header">
              <span class="cases__item--header-text">Заказчик:</span>
              <h2 class="cases__item--header-title">{{ item.title }}</h2>
            </div>
            <div class="cases__items--tools">
              <div class="cases__item--task cases__item-same">
                <span>Задача:</span>
                <h3>{{ item.task }}</h3>
              </div>
              <div class="cases__item--tool cases__item-same">
                <span>Инструмент:</span>
                <h3>{{ item.tool }}</h3>
              </div>
              <div class="cases__item--platform cases__item-same">
                <span>Платформа:</span>
                <h3>{{ item.platform }}</h3>
              </div>
              <div class="cases__item--budget cases__item-same">
                <span>Рекламный бюджет:</span>
                <p>{{ item.budget }}</p>
              </div>
              <div class="cases__item--result cases__item-same">
                <span>Результат:</span>
                <p>{{ item.result }}</p>
              </div>
            </div>
          </div>
        </div>
      </VueSlickCarousel>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Cases",
    data () {
      return {
        slickOptions: {
          slidesToShow: 3,
          focusOnSelect: true,
          infinite: true,
          autoplay: true,
          autoplaySpeed: 5000,
          speed: 1000,
          arrows: false,
          responsive: [
            {
              breakpoint: 960,
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
            title: 'IT школа для детей',
            task: 'привлечение новых учеников для формирование групы по новому направлению.',
            tool: 'таргетированая реклама',
            platform: 'Facebook & Instagram',
            budget: '130 долларов США',
            result: '34 заявки за 2 недели, на общую сумму 8933 доларов США.'
          },
          {
            title: 'Компания VETER',
            task: 'привлечение новых, потенциальных клиентов, путем генерации лидов на сайте.',
            tool: 'таргетированая реклама',
            platform: 'Facebook & Instagram',
            budget: '150 долларов США',
            result: '53 заявки за месяц, из которых была сделана продажа на 12500 доларов США, остальные заявки в работе.'
          },
          {
            title: 'Магазин мебели SHADEKO',
            task: 'увеличение продаж, путем привлечения заинтересованых клиентов через Instagram direct.',
            tool: 'таргетированая реклама',
            platform: 'Instagram',
            budget: '500 долларов США',
            result: 'За весь период рекламной кампании получено 548 заявок.'
          },
          {
            title: 'Альтпапир',
            task: 'повысить узнаваемость бренда, а также увеличить трафик на сайт',
            tool: 'таргетированая реклама',
            platform: 'Facebook & Instagram',
            budget: '300 долларов США',
            result: 'охват аудитории 240000, 7000 посетителей сайта, 7% оставили заявку'
          },
          {
            title: 'BSG',
            task: 'без использования рекламы, повысить вовлеченность аудитории, заинтересовать потенциальных клиентов',
            tool: 'SMM',
            platform: 'Facebook & Instagram',
            budget: '100 долларов США/месяц',
            result: 'вовлеченность аудитории выросла на 250%, за 2 месяца получили 8 заявок на потенциальное сотрудничество'
          },
          {
            title: 'Интернет-магазин по продаже фильтров для тяжелой и строительной техники',
            task: 'увеличить поисковой трафик из Google; Продвинуть определенную группу запросов в ТОП-10 результатов выдачей',
            tool: 'SEO',
            platform: 'Google Search',
            budget: '550 долларов США/месяц',
            result: 'трафик сайта с органических поисковых запросов вырос в 7 раз'
          },
          {
            title: 'Интернет-магазина Pilti.ua ',
            task: 'увеличение продаж; увеличение повторных продаж; повысить узнаваемость бренда',
            tool: 'SEO|SMM|PPC|Re-design',
            platform: 'Google Search, Facebook & Instagram, Google ADS',
            budget: '950 долларов США/месяц',
            result: 'благодаря комплексу действий были увеличены продажи на 74,3%, по сравнению с результатами предыдущего года'
          },
          {
            title: 'Интернет-магазина строительного оборудования ',
            task: 'увеличение продаж, путем привлечения горячих лидов через Гугл',
            tool: 'PPC',
            platform: 'Google ADS',
            budget: '1200 долларов США',
            result: 'CTR ~ 9 %; Конверсий - 45; Стоимость конверсии -29$; Средний чек - 900 $; 5 продаж '
          },
        ]
      }
    }
  }
</script>

<style scoped>
  .cases__block {
    background-image: url("/cases-bg.webp");
    background-repeat:no-repeat;
    -webkit-background-size:cover;
    -moz-background-size:cover;
    -o-background-size:cover;
    background-size:cover;
    background-position:center;
  }
  .cases__block--wrapper {
    display: flex;
    height: 100vh;
    background-color: rgba(0, 0, 0, .8);
  }
  .cases__title {
    letter-spacing: 15px;
    text-align: center;
    margin: auto;
    font-size: 62px;
    text-transform: uppercase;
  }

  @media screen and (max-width: 600px) {
    .cases__title {
      font-size: 45px;
      letter-spacing: 5px;
    }
  }

  .cases__wrapper {
    margin-top: -220px;
    padding-left: 40px;
    padding-right: 40px;
    position: relative;
  }
  .cases__item--list {
    margin-bottom: 75px !important;
    max-width: 450px;
    background-color: #2f6464;
    display: flex;
    margin: 0 -10px;
    box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
  }
  .cases__item--item {
    margin: 0 10px;
  }
  .cases__items--tools {
    padding: 0 10px 10px 45px;
  }
  .cases__item--header {
    margin: 0 auto;
    text-align: center;
    padding-top: 30px;
  }
  .cases__item--header-text {
    font-size: 28px;
    color: #f8f8f1;
  }
  .cases__item--header-title {
    font-size: 22px;
    font-weight: normal;
    line-height: 25px;
  }
  .cases__item-same span {
    display: block;
    font-size: 16px;
    margin-top: 40px;
  }
  .cases__item-same h3,
  .cases__item-same p {
    font-size: 13px;
    font-weight: normal;
  }
  ::v-deep .slick-slider {
    /*position: relative;*/
    overflow: hidden;
  }
  ::v-deep .slick-track {
    display: flex;
    justify-content: space-between;
  }
  ::v-deep .slick-slide {
    padding: 0 30px;
    display: flex;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
  }

  ::v-deep .slick-arrow {
    position: absolute;
    top: 50%;
    /*margin: -30px 0px 0px 0px;*/
    z-index: 10;
    font-size: 0;
    width: 30px;
    height: 60px;
  }

  ::v-deep .slick-prev {
    left: 5px;
    background: url('/sl-arrow_l.svg') 0 0 / 100% no-repeat;
    z-index: 1;
  }

  ::v-deep .slick-next {
    right: 5px;
    background: url('/sl-arrow_r.svg') 0 0 / 100% no-repeat;
    z-index: 1;
  }

  @media (max-width:600px) {
    .cases__item--list {
      margin: 0;
    }
    .cases__item--item {
      margin: 0;
    }
  }
</style>
