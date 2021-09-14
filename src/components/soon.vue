<template>
  <div class="wrapper">
    <div class="pink-rectangle"></div>
    <div class="images">
      <img class="donuts" src="../assets/images/soon/donuts.png" />
      <img class="cake" src="../assets/images/soon/cake.png" />
    </div>
    <div class="text">
      <p class="text-content">USKORO: <br />SLATKOTEKA <br />NOVI BEOGRAD</p>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  margin-top: 112px;
  padding-left: 151px;
  padding-right: 151px;
  width: 100%;
  height: 450px;
  position: relative;
}

.pink-rectangle {
  height: 364px;
  transform: rotate(-4deg);
  box-shadow: 0 1px 9px 0 rgba(0, 35, 64, 0.2);
  background-color: #f650a0;
  position: absolute;
  top: 45px;
  right: 163px;
  left: 198px;
}

.images {
  position: absolute;
  display: flex;
  align-items: flex-start;
  top: 0;
  left: 151px;
  z-index: 2;
  width: 60%;
  height: 100%;
}

.donuts {
  margin-right: 27px;
}

.cake {
  align-self: flex-end;
  margin-right: 67px;
  margin-bottom: -35px;
}

.text {
  position: absolute;
  right: 151px;
  top: 121px;
  width: 30%;
}

.text-content {
  font-size: 45px;
  line-height: 1.22;
  letter-spacing: 0.15px;
  color: white;
}
</style>