<template>
  <div class="hero text-center" style="height: 100%">
    <h1 class="hero__title">EisakuBoon!!</h1>
    <p class="hero__description">
      毎日の英作文トレーニングを通して
      <br />
      英語のスピーキング能力を鍛えよう
    </p>
    <p class="hero__message">Choose a course</p>
    <div class="text-center">
      <v-btn
        outlined
        large
        color="#fff"
        width="50%"
        to="training"
        class="course__item"
      >
        英会話
      </v-btn>
    </div>
  </div>
</template>

<style>
.hero {
  background: -moz-linear-gradient(top, #34558b 30%, #ff6f61 100%);
  background: -webkit-linear-gradient(top, #34558b 30%, #ff6f61 100%);
  background: linear-gradient(to bottom, #34558b 30%, #ff6f61 100%);
}
.hero__title {
  color: #fff;
  font-family: 'Fugaz One';
  margin: 100px 0;
  font-size: 3rem;
}
.hero__description {
  color: #fff;
  font-weight: bold;
  font-family: 'M PLUS Rounded 1c';
  margin-bottom: 100px;
}
.hero__message {
  color: #fff;
  font-family: 'Fugaz One';
  font-size: 1.5rem;
}
</style>
