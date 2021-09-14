<template>
  <div>
    <nav class="rectangle">
      <img class="Group-11" src="../assets/images/logo.svg" />
      <ul class="link-list">
        <li class="link" v-for="item in links" :key="item.name">
          <a class="link-item" :href="item.link">{{ item.name }}</a>
        </li>
      </ul>
      <div class="right-content">
        <div class="lang">
          <span class="lang-srb">SRB</span>/<span class="lang-eng">ENG</span>
        </div>
        <div class="items-container">
          <img src="../assets/images/shoping-bag.svg" /><span class="item-num"
            >(1)</span
          >
        </div>
      </div>
    </nav>
    <div class="curvy-line">
      <div class="header-content">
        <h1 class="title">LOKACIJE</h1>
        <p class="header-text">
          Savršen spoj ukusa i dekoracije koji za tebe izdvajaju naši
          krofnoslastičari. Vazdušasto testo smo prelili finom belom čokoladom,
          dok smo u središte najfinijeg zalogaja smestili kinder jaje ispunjeno
          kremastim kinder filom i sočnom jagodom.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["links"],
};
</script>

<style scoped>
.rectangle {
  width: 100%;
  height: 70px;
  padding: 0 151px;
  background-color: #ffebf2;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

img.Group-11 {
  width: 128px;
  height: 35px;
  object-fit: contain;
}

.link-list {
  display: flex;
  list-style: none;
}

.link {
  margin: 0 10px;
}

.lang,
.item-num {
  font-size: 15px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.05px;
  color: #000000;
}

.right-content {
  display: flex;
}

.items-container {
  margin-left: 20px;
  display: flex;
  align-items: center;
}

.lang-srb,
.item-num {
  color: #f650a0;
}

.curvy-line {
  position: relative;
  padding: 0 151px;
  width: 100%;
  height: 267px;
  padding: 0 0 45px;
  object-fit: contain;
  background: url("../assets/images/curvy-line.svg");
  background-position: bottom;
}

.header-content {
  position: absolute;
  top: 78px;
  left: 151px;
  width: 60%;
}

.title {
  font-size: 55px;
  letter-spacing: 0.18px;
  color: #000000;
}

.header-text {
  font-family: "Varela Round";
  font-size: 16px;
  line-height: 1.25;
  letter-spacing: 0.05px;
  color: #000000;
}
</style>
