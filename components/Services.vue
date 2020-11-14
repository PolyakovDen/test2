<template>
  <div class="services">
    <div class="services__header elevation-20">
      <h2 class="services__header--item">Наши услуги</h2>
    </div>
    <div class="services__list--wrapper">
      <v-container fluid class="pa-0">
        <div class="services__list mr-2 ml-2 d-flex justify-center flex-wrap">
          <ServicesCard
            v-for="(item, index) in items"
            :key="index"
            :item="item"
            class="services__item"
          />
        </div>
      </v-container>
    </div>
  </div>
</template>

<script>
  import ServicesCard from "~/components/ServicesCard";
  export default {
    name: "Services",
    components: {
      ServicesCard
    },
    data () {
      return {
        items: [
          {
            src: 'social-media.png',
            description: 'Социальные сети',
            title: 'Продвижение в социальных сетях',
            descriptionItems: [
              {
                item: 'создание маркетинговой стратегии продвижения'
              },
              {
                item: 'создание контент-стратегии'
              },
              {
                item: 'создание уникального контента'
              },
              {
                item: 'создание, оформление и наполнение Instagram и Facebook страниц'
              },
              {
                item: 'работа с блогерами'
              },
              {
                item: 'создание и ведение таргетированой рекламы'
              }
            ]
          },
          {
            src: 'pay-per-click.png',
            description: 'Контекстная реклама',
            title: 'Контекстная реклама',
            descriptionItems: [
              {
                item: 'создание маркетинговой стратегии продвижения'
              },
              {
                item: 'создание контент-стратегии'
              },
              {
                item: 'создание уникального контента'
              },
              {
                item: 'создание, оформление и наполнение Instagram и Facebook страниц'
              },
              {
                item: 'работа с блогерами'
              },
              {
                item: 'создание и ведение таргетированой рекламы'
              }
            ]
          },
          {
            src: 'gear.png',
            description: 'SEO оптимизация',
            title: 'SEO оптимизация',
            descriptionItems: [
              {
                item: 'создание маркетинговой стратегии продвижения'
              },
              {
                item: 'создание контент-стратегии'
              },
              {
                item: 'создание уникального контента'
              },
              {
                item: 'создание, оформление и наполнение Instagram и Facebook страниц'
              },
              {
                item: 'работа с блогерами'
              },
              {
                item: 'создание и ведение таргетированой рекламы'
              }
            ]
          },
          {
            src: 'letter.png',
            description: 'Email маркетинг',
            title: 'Email маркетинг',
            descriptionItems: [
              {
                item: 'создание маркетинговой стратегии продвижения'
              },
              {
                item: 'создание контент-стратегии'
              },
              {
                item: 'создание уникального контента'
              },
              {
                item: 'создание, оформление и наполнение Instagram и Facebook страниц'
              },
              {
                item: 'работа с блогерами'
              },
              {
                item: 'создание и ведение таргетированой рекламы'
              }
            ]
          },
          {
            src: 'programming.png',
            description: 'Web разработка',
            title: 'Web разработка',
            descriptionItems: [
              {
                item: 'создание маркетинговой стратегии продвижения'
              },
              {
                item: 'создание контент-стратегии'
              },
              {
                item: 'создание уникального контента'
              },
              {
                item: 'создание, оформление и наполнение Instagram и Facebook страниц'
              },
              {
                item: 'работа с блогерами'
              },
              {
                item: 'создание и ведение таргетированой рекламы'
              }
            ]
          },
          {
            src: 'web-design.png',
            description: 'Web дизайн',
            title: 'Web дизайн',
            descriptionItems: [
              {
                item: 'создание маркетинговой стратегии продвижения'
              },
              {
                item: 'создание контент-стратегии'
              },
              {
                item: 'создание уникального контента'
              },
              {
                item: 'создание, оформление и наполнение Instagram и Facebook страниц'
              },
              {
                item: 'работа с блогерами'
              },
              {
                item: 'создание и ведение таргетированой рекламы'
              }
            ]
          },
          {
            src: 'sell.png',
            description: 'Оптимизация продаж',
            title: 'Оптимизация продаж',
            descriptionItems: [
              {
                item: 'создание маркетинговой стратегии продвижения'
              },
              {
                item: 'создание контент-стратегии'
              },
              {
                item: 'создание уникального контента'
              },
              {
                item: 'создание, оформление и наполнение Instagram и Facebook страниц'
              },
              {
                item: 'работа с блогерами'
              },
              {
                item: 'создание и ведение таргетированой рекламы'
              }
            ]
          },
          {
            src: 'content.png',
            description: 'Контент маркетинг',
            title: 'Контент маркетинг',
            descriptionItems: [
              {
                item: 'создание маркетинговой стратегии продвижения'
              },
              {
                item: 'создание контент-стратегии'
              },
              {
                item: 'создание уникального контента'
              },
              {
                item: 'создание, оформление и наполнение Instagram и Facebook страниц'
              },
              {
                item: 'работа с блогерами'
              },
              {
                item: 'создание и ведение таргетированой рекламы'
              }
            ]
          }
        ]
      }
    }
  }
</script>

<style scoped>
  .services__header {
    padding-top: 45px;
    padding-bottom: 45px;
    text-align: center;
  }

  .services__header--item {
    font-size: 62px;
    text-transform: uppercase;
    letter-spacing: 15px;
  }

  @media screen and (max-width: 600px) {
    .services__header--item {
      font-size: 45px;
      letter-spacing: 5px;
    }
  }

  .container {
    max-width: 1000px !important;
  }

  .services__list {
    margin-top: 55px;
    margin-bottom: 120px;
  }

  .services__list:first-child {
    margin-bottom: 0;
  }

  .services__item {
    margin-right: 65px;
  }

  @media (max-width:600px) {
    .services__item {
      margin-right: 35px;
    }
  }

  @media (max-width:450px) {
    .services__item {
      margin-right: 20px;
    }
  }
</style>
