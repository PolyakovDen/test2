<template>
  <div class="advantages">
    <h2 class="advantages__title" data-aos="flip-up">
      Преимущества компании
    </h2>
    <div class="mb-10 advantages__list d-flex justify-space-around flex-wrap">
      <div data-aos="flip-right" data-aos-duration="700" data-aos-easing="ease-in-sine" v-for="(item, i) in items" :key="i" class="advantages__item">
        <div class="flip-card mb-5">
          <div class="flip-card-inner">
            <div class="flip-card-front">
              <img class="flip-card-front--img" :src="item.src" alt="" width="160" height="160">
            </div>
            <div class="flip-card-back">
              <h1>{{ item.text }}</h1>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Advantages',
  data () {
    return {
      items: [
        {
          text: 'Несем финансовую ответственность за результат',
          src: 'money.png'
        },
        {
          text: 'Умножаем не только заявки, но и продажи',
          src: 'sales.png'
        },
        {
          text: 'Предоставляем комплекс услуг по продвижению',
          src: 'social.png'
        },
        {
          text: 'Обеспечиваем поддержку по завершению проекта',
          src: 'support.png'
        }
      ]
    }
  }
}
</script>

<style scoped>
  .advantages {
    max-width: 1000px;
    margin: 0 auto;
  }

  .advantages__title {
    letter-spacing: 15px;
    text-align: center;
    margin: auto;
    font-size: 62px;
    text-transform: uppercase;
  }

  @media screen and (max-width: 900px) {
    .advantages__title {
      font-size: 55px;
    }
  }
  @media screen and (max-width: 600px) {
    .advantages__title {
      font-size: 37px;
      letter-spacing: 5px;
    }
  }
  @media screen and (max-width: 340px) {
    .advantages__title {
      word-wrap: break-word;
    }
  }

  .advantages__list {
    margin-top: 80px;
  }

  .flip-card {
    background-color: transparent;
    width: 220px;
    height: 220px;
    perspective: 1000px;
  }

  .flip-card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: transform 0.6s;
    transform-style: preserve-3d;
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  }

  .flip-card:hover .flip-card-inner {
    transform: rotateY(180deg);
  }

  .flip-card-front, .flip-card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
  }

  .flip-card-front {
    display: flex;
    justify-content: center;
    align-items: center;
    box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
    color: black;
  }

  .flip-card-back {
    padding-top: 30px;
    font-size: 12px;
    color: white;
    box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
    transform: rotateY(180deg);
  }
</style>
