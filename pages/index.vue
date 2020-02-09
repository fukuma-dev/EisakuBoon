<template>
  <div class="hero" style="height: 100%">
    <h1 class="hero__title">EisakuBoon!!</h1>
    <p class="hero__message">Choose a course</p>
    <div class="text-center">
      <v-btn flat outlined large color="#fff" width="50%" to="training">
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
  text-align: center;
  color: #fff;
  font-family: 'Fugaz One';
  margin: 100px 0;
  font-size: 3rem;
}
.hero__message {
  text-align: center;
  color: #fff;
  font-family: 'Fugaz One';
  margin: 100px 0;
  font-size: 1.5rem;
}
</style>
