<template>
  <div class="splashBody">
    <div>
      <h1 class="hero">Food ordering just got a whole lot easier.</h1>
      <p class="heroText">
        This app was built with VueJS by Nang Aye Bo Kham. The app allows user to add thier preferable items into the cart and automatically provide the bill. The idea is adopted by the food ordering assest from Mc Donald's, etc which helps customers to order their own items without the waiters. This way, the user will get high tech enviroment just dining in the restaurant or any order related stores.
      </p>
    </div>
    <img src="../assets/splash.svg" class="splashImage" alt="splash" />
  </div>
</template>

<style scoped>
.hero {
  max-width: 600px;
  font-family: Outfit;
}
.splashBody {
  display: flex;
  gap: 40px;
  align-items: center;
  justify-content: center;
  font-size: 40px;
  max-width: 1440px;
  padding: 20px;
  min-height: calc(100vh - 120px);
  margin: 0px;
  padding-bottom: 40px;
}
.heroText {
  font-family: Inter;
  font-size: 24px;
  font-weight: 200;
  line-height: 1.5em;
}
.splashImage {
  height: 400px;
}
@media (max-width: 1200px) {
  .splashImage {
    height: 300px;
  }
}
@media (max-width: 900px) {
  .splashImage {
    height: unset;
    width: 100%;
  }
  .splashBody {
    flex-direction: column;
  }
}
</style>