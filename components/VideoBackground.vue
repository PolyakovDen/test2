<template>
  <div class="" id="main">
    <div class="hidden-sm-and-down bg-video__wrapper">
      <div class="bg-video">
        <h1 class="main__title">
          Мы готовы помочь вашему бизнесу
          выйти на новый уровень, не смотря на то,
          какой бюджет вы готовы выделять на это
        </h1>
      </div>
      <video class="background-video" poster="/header-bg.webp" autoplay muted loop>
        <source src="/video.mp4" type="video/mp4">
      </video>
    </div>
    <div class="bg-without-video__wrapper hidden-md-and-up">
      <div class="bg-without-video">
        <h1 class="main__title">
          Мы готовы помочь вашему бизнесу
          выйти на новый уровень, не смотря на то,
          какой бюджет вы готовы выделять на это
        </h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'VideoBackground'
}
</script>

<style scoped>
  .bg-video__wrapper {
    position: relative;
  }

  .background-video {
    width: 100%;
    height: 100%;
  }

  .background-video video {
    width: 100%;
    height: 100%;
  }

  .bg-without-video__wrapper {
    background-image: url("/header-bg.webp");
    background-repeat:no-repeat;
    -webkit-background-size:cover;
    -moz-background-size:cover;
    -o-background-size:cover;
    background-size:cover;
    background-position:center;
  }

  .bg-video {
    position: absolute;
    display: flex;
    height: 100%;
    width: 100%;
    background-color: rgba(0, 0, 0, .7);
  }

  .bg-without-video {
    display: flex;
    height: 100vh;
    background-color: rgba(0, 0, 0, .8);
  }

  .main__title {
    background-color: rgba(255, 255, 255, .3);
    color: rgba(0, 0, 0, .8);
    border-radius: 10px;
    width: 90%;
    text-align: center;
    margin: auto;
  }
</style>
