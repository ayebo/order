<template>
  <div class="header">
    <NuxtLink to="/">
      <h1 class="headerTitle">Sharon Nang</h1>
    </NuxtLink>
    <NuxtLink to="/order">
      <div class="navButton navButton--glow">Order Now</div>
    </NuxtLink>
  </div>
</template>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  font-family: Outfit;
  align-items: center;
  box-shadow: inset 0 0 2000px rgba(255, 255, 255, 0.5);
  padding: 20px;
  height: 120px;
}
.headerTitle {
  font-weight: 200;
  text-align: center;
  margin: 0px;
  color: rgb(30, 12, 112);
}

.navButton {
  min-width: 220px;
  padding: 18px 25px;
  cursor: pointer;
  position: relative;
  font-weight: 700;
  background: black;
  color: #fff;
}

.navButton--glow {
  z-index: 1;
  transition: all 0.3s ease-out;
  border-radius: 10px;
}

.navButton--glow:before {
  content: '';
  background: linear-gradient(
    45deg,
    #ff3c3c,
    #4968ff,
    #a34dff,
    #ff53da,
    #ff4444
  );
  position: absolute;
  top: 0;
  left: 0;
  background-size: 400%;
  z-index: -1;
  animation: glowing 20s linear infinite;
  opacity: 0;
  transition: all 0.3s ease-out;
  border-radius: 10px;
  transform-origin: center;
  transform: translateZ(0);
  width: 100%;
  height: 100%;
}

.navButton--glow:hover {
  transform: scale(1.025) translateZ(0);
}
.navButton--glow:hover:before {
  opacity: 1;
  transform: translateZ(0) scaleX(1.045) scaleY(1.145);
}
.navButton--glow:active::after {
  background: rgb(36, 36, 36);
}

.navButton--glow:after {
  z-index: -1;
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  background: black;
  left: 0;
  top: 0;
  border-radius: 8px;
}
@media (max-width: 500px) {
  .headerTitle {
    margin-bottom: 20px;
  }
  .header {
    flex-direction: column;
    height: unset;
  }
}
</style>

