<template>
  <div class="wrapper">
    <img class="line-1" src="../assets/images/footer/line-1.svg" />
    <img class="line-2" src="../assets/images/footer/line-2.svg" />
    <img class="donut" src="../assets/images/footer/donut.png" />
    <p class="prava">
      © 2017-2020 Slatkoteka | Sva prava zadržana | dev, dizajn, marketing:
      Avokado.rs
    </p>
    <div class="media">
      <img src="../assets/images/footer/logo.svg" />
      <p>Prva specijalizovana prodavnica krofni i kronata u Srbiji.</p>
      <div class="social-media">
        <img src="../assets/images/footer/social-1.png" />
        <img src="../assets/images/footer/social-2.png" />
        <img src="../assets/images/footer/social-3.png" />
      </div>
    </div>

    <div class="footer-nav">
      <ul>
        <li v-for="item in links" :key="item.link">
          <a class="link-item" :href="item.link">{{ item.name }}</a>
          <p>{{ item.text }}</p>
        </li>
      </ul>
    </div>

    <div class="join">
      <span>Postani deo Slatkoteka tima</span>
      <a class="job-link" href="https://slatkoteka.rs/posao/"
        >PRIJAVA ZA POSAO</a
      >
    </div>
  </div>
</template>

<script>
export default {
  props: ["links"],
};
</script>

<style scoped>
.wrapper {
  width: 100%;
  height: 345px;
  padding: 67px 248px 39px 139px;
  box-shadow: 0 1px 9px 0 rgba(0, 35, 64, 0.2);
  background-color: #ffebf2;
  position: relative;
  display: flex;
  justify-content: space-around;
}

.line-1 {
  position: absolute;
  left: 0;
  bottom: 0;
}

.line-2 {
  position: absolute;
  bottom: 0;
  right: 364px;
}

.donut {
  position: absolute;
  right: 0;
  bottom: 0;
}

.media {
  width: 25%;
  display: flex;
  flex-direction: column;
}

.media img {
  width: 175px;
}

.media p {
  margin: 17px 0;
  font-family: "Varela Round";
  font-size: 14px;
}

.social-media img {
  margin-right: 20px;
  height: 25px;
  width: 25px;
}

.footer-nav {
  width: 30%;
}

ul,
li {
  width: 100%;
}

li {
  display: flex;
  justify-content: space-between;
  margin-bottom: 10px;
}

li span {
  font-size: 15px;
  font-weight: bold;
  letter-spacing: 0.05px;
}

li p {
  text-align: left;
  width: 60%;
  font-family: "Varela Round";
  font-size: 14px;
}

.join span {
  display: block;
  margin-bottom: 16px;
  font-family: "Varela Round";
  font-size: 14px;
  color: #f454a0;
}

.join a {
  text-decoration: none;
  padding: 5px 6px 5px 7px;
  border-radius: 1.9px;
  background-color: #f454a0;
  font-size: 14px;
  text-align: center;
  color: white;
  transition: all 0.2s ease;
}

.job-link:hover,
.job-link:active {
  transform: scale(2);
}

.prava {
  font-family: "Varela Round";
  font-size: 12px;
  color: #656565;
  position: absolute;
  left: 138px;
  bottom: 28px;
}
</style>