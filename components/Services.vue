<template>
  <div class="services" id="services">
    <div class="services__header elevation-20">
      <h2 class="services__header--item" data-aos="flip-up">
        Наши услуги
      </h2>
    </div>
    <div class="services__list--wrapper">
      <v-container fluid class="pa-0">
        <div class="test">
          <div class="services__list mr-2 ml-2">
            <ServicesCard
              v-for="(item, index) in items"
              :key="index"
              :item="item"
              class="services__item"
            />
          </div>
        </div>
      </v-container>
    </div>
  </div>
</template>

<script>
import ServicesCard from '~/components/ServicesCard'
export default {
  name: 'Services',
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
              item: '- создание маркетинговой стратегии продвижения'
            },
            {
              item: '- создание контент-стратегии'
            },
            {
              item: '- создание уникального контента'
            },
            {
              item: '- создание, оформление и наполнение Instagram и Facebook страниц'
            },
            {
              item: '- работа с блогерами'
            },
            {
              item: '- создание и ведение таргетированой рекламы'
            }
          ]
        },
        {
          src: 'pay-per-click.png',
          description: 'Контекстная реклама',
          title: 'Контекстная реклама Google & Яндекс',
          descriptionItems: [
            {
              item: '- разработка отдельной кампании под РСЯ и Google Ads'
            },
            {
              item: '- выборка конверсионных ключевых фраз'
            },
            {
              item: '- ручное составление заголовков и текстов объявлений'
            },
            {
              item: '- настройка быстрых ссылок и привязка к ним UTM-меток'
            },
            {
              item: '- настройка гео и временного таргетинга'
            },
            {
              item: '- настройка Целей и Яндекс Метрике и Google Analytics'
            }
          ]
        },
        {
          src: 'gear.png',
          description: 'SEO оптимизация',
          title: 'Поисковая оптимизация сайтов',
          descriptionItems: [
            {
              item: '- первичный SEO-аудит'
            },
            {
              item: '- устранение ошибок на сайте'
            },
            {
              item: '- настройка плагинов'
            },
            {
              item: '- формирование семантического ядра'
            },
            {
              item: '- внешняя поисковая оптимизация'
            },
            {
              item: '- вывод сайта в ТОП по нужным поисковым запросам'
            }
          ]
        },
        {
          src: 'letter.png',
          description: 'Email маркетинг',
          title: 'Email-маркетинг',
          descriptionItems: [
            {
              item: '- создание и внедрение Email-стратегии'
            },
            {
              item: '- построение эффективного сбора и актуализации базы подписчиков / клиентов'
            },
            {
              item: '- сегментация целевых групп'
            },
            {
              item: '- персонализаця сообщений'
            },
            {
              item: '- работа по повышению конверсийности в каналах Email и мессенджерах'
            }
          ]
        },
        {
          src: 'programming.png',
          description: 'Web разработка',
          title: 'Разработка сайтов под ключ',
          descriptionItems: [
            {
              item: '- анализ сайтов конкурентов'
            },
            {
              item: '- создание уникального контента для сайта'
            },
            {
              item: '- создание структуры сайта'
            },
            {
              item: '- разработка персонализированного дизайна сайта'
            },
            {
              item: '- разработка сайта командой программистов'
            },
            {
              item: '- базовые настройки SEO'
            },
            {
              item: '- обеспечение хостинга и домена'
            }
          ]
        },
        {
          src: 'web-design.png',
          description: 'Web дизайн',
          title: 'Разработка дизайнов для сайта',
          descriptionItems: [
            {
              item: '- формирование индивидуального стиля'
            },
            {
              item: '- разработка структуры сайта'
            },
            {
              item: '- создание уникального визуального контента для сайта'
            },
            {
              item: '- написание текстов'
            },
            {
              item: '- разработка UI/UX элементов'
            },
            {
              item: '- разработка непосредственно дизайна, с адаптацией под разные виды устройств'
            }
          ]
        },
        {
          src: 'sell.png',
          description: 'Оптимизация продаж',
          title: 'Оптимизация продаж',
          descriptionItems: [
            {
              item: '- интегрция с CRM системой'
            },
            {
              item: '- техники эффективных продаж'
            },
            {
              item: '- технологии переговорного процесса'
            },
            {
              item: '- разработка скриптов продаж'
            },
            {
              item: '- работа с возраждениями'
            },
            {
              item: '- шаблоны для переписок'
            },
            {
              item: '- интеграция с ІP телефонией'
            },
            {
              item: '- разработка воронки продаж'
            }
          ]
        },
        {
          src: 'content.png',
          description: 'Контент маркетинг',
          title: 'Контент-маркетинг',
          descriptionItems: [
            {
              item: 'Включает в себя создание и обработку:'
            },
            {
              item: '- фото контента'
            },
            {
              item: '- видео контента'
            },
            {
              item: '- текстового контента'
            },
            {
              item: '- аудио контента'
            },
            {
              item: '- графического контента'
            },
            {
              item: '- мультимедийного контента'
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

  .test {
    margin: 0 auto;
    max-width: 700px;
    display: flex;
  }

  .services__list {
    margin-top: 55px;
    margin-bottom: 120px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }

  .services__list:first-child {
    margin-bottom: 0;
  }

  /*.services__item {*/
  /*  margin-right: 65px;*/
  /*}*/

  @media (max-width:600px) {
    .services__item {
      margin-right: 35px;
    }
  }

  @media (max-width:450px) {
    .services__item {
      margin-right: 20px;
    }
    .services__list {
      justify-content: center;
    }
  }
</style>
