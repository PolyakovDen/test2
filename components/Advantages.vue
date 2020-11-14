<template>
  <div class="advantages">
    <h2 class="advantages__title">
      Преимущества компании
    </h2>
    <div class="advantages__list d-flex justify-space-around flex-wrap">
      <div class="advantages__item" v-for="(item, i) in items" :key="i">
        <div class="flip-card mb-5">
          <div class="flip-card-inner">
            <div class="flip-card-front">
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
    name: "Advantages",
    data () {
      return {
        items: [
          {
            text: 'Hello from Den'
          },
          {
            text: 'Hello from Stas'
          },
          {
            text: 'lorem lorem lorem lorem'
          },
          {
            text: 'Hello from ipsum ipsum'
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

  @media screen and (max-width: 600px) {
    .advantages__title {
      font-size: 45px;
      letter-spacing: 5px;
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
    background-color: #bbb;
    color: black;
  }

  .flip-card-back {
    background-color: #2980b9;
    color: white;
    transform: rotateY(180deg);
  }
</style>
