<template>
  <div id="lokacije" class="container">
    <p>
      <span class="Poetna-Lokacije Text-Style-5">
        Početna >><span class="text-style-1">Lokacije</span>
      </span>
    </p>
    <ul>
      <li class="store" v-for="(store, index) in locations" :key="index">
        <div class="left-side">
          <h2 class="store-name">
            <img class="location-image" src="../assets/images/location.svg" />{{
              store.name
            }}
          </h2>
          <div class="info">
            <div class="kontakt">
              <h4>KONTAKT:</h4>
              <p class="kontakt-info">
                {{ store.address }} <br />
                {{ store.phone }}, Viber, WhatsApp
              </p>
              <p class="working">
                Svakog radnog dana {{ store.workDays }} <br />
                Vikendom {{ store.weekends }}
              </p>
            </div>

            <div class="dostupno">
              <h4>DOSTUPNO</h4>
              <ul class="items-available">
                <li
                  class="available-item"
                  v-for="(product, index) in store.products"
                  :key="index"
                  :style="{ background: product.background }"
                >
                  <h5>
                    {{ product.name }}
                  </h5>
                </li>
              </ul>
            </div>
          </div>
          <div class="middle">
            <span class="line"></span>
            <p>*obavezno poručivanje unapred</p>
          </div>
          <div class="store-pictures">
            <ul class="image-list">
              <li v-for="(img, index) in store.images" :key="index">
                <span class="store-image-container">
                  <img
                    class="store-image"
                    :src="
                      require('../assets/images/slatkoteka-images/img-' +
                        img +
                        '.png')
                    "
                  />
                </span>
              </li>
            </ul>
          </div>
        </div>
        <div class="right-side">
          <span class="map" v-html="store.map"></span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      locations: [
        {
          name: "SLATKOTEKA DORĆOL (CENTAR)",
          address: "Višnjićeva 5, Beograd",
          phone: "065 33 00 508",
          workDays: "09 do 22",
          weekends: "10 do 22",
          products: [
            { name: "KROFNE", background: "#ffebf2" },
            { name: "SLATKOLADE", background: "#a3e8d6" },
            { name: "SLATKOTEKA IZNENAĐENJA*", background: "#fcfa96" },
          ],
          map: '<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2830.0454905423862!2d20.456495615751066!3d44.82063788417375!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x475a654b4a8cca67%3A0x9327aa24208729d1!2sSlatkoteka!5e0!3m2!1sen!2srs!4v1631121456709!5m2!1sen!2srs" allowfullscreen="" loading="lazy"></iframe>',
          images: [1, 2, 3, 4],
        },
        {
          name: "SLATKOTEKA 3",
          address: "Bulevar kralja Aleksandra 52, Beograd",
          phone: "065 33 00 521",
          workDays: "09 do 22",
          weekends: "10 do 22",
          products: [
            { name: "KROFNE", background: "#ffebf2" },
            { name: "SLATKOLADE", background: "#a3e8d6" },
            { name: "KAPKEJKS", background: "#e0c5ec" },
            { name: "SLATKOTEKA IZNENAĐENJA*", background: "#fcfa96" },
          ],
          map: '<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2830.671238707512!2d20.467714715750713!3d44.807888285015174!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x475a7b6baafee44d%3A0x2b5bc9450faea7ae!2sSlatkoteka%203!5e0!3m2!1sen!2srs!4v1631121778784!5m2!1sen!2srs" allowfullscreen="" loading="lazy"></iframe>',
          images: ["1", "2", "3", "4"],
        },
      ],
    };
  },
};
</script>

<style scope>
.Poetna-Lokacije {
  font-family: "Varela Round";
  font-size: 12px;
  color: #999999;
}
.Poetna-Lokacije .text-style-1 {
  color: #000000;
}

.store {
  display: flex;
  justify-content: space-between;
  font-family: "Varela Round";
  width: 100%;
  margin-top: 40px;
  padding-left: 41px;
  box-shadow: 0 1px 9px 0 rgba(0, 35, 64, 0.2);
  background-color: #ffffff;
}

.left-side {
  width: 50%;
}

.store-name {
  margin-top: 38px;
  padding-bottom: 12px;
  border-bottom: solid 1.2px #e7e7e7;
  font-size: 22px;
  letter-spacing: 0.07px;
}

.location-image {
  margin-right: 8px;
}

.info {
  display: flex;
  margin-top: 16px;
}

.kontakt {
  width: 50%;
  margin-right: 29px;
  display: flex;
  flex-direction: column;
}

.kontakt h4 {
  margin-bottom: 8px;
}

.kontakt-info {
  text-decoration: underline;
}

.working {
  margin-top: 16px;
  text-decoration: underline;
}

.dostupno {
  width: 50%;
}

h5 {
  font-size: 14px;
}

.items-available {
  margin-top: 5px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.available-item {
  padding: 3px 6px;
  color: #000000;
  font-size: 12.9px;
  margin-left: 9px;
  margin-bottom: 12px;
}

.right-side {
  width: 40%;
}

.map {
  width: 50%;
  overflow: hidden;
}

iframe {
  width: 100%;
  height: 100%;
  border: 0;
}

.store-pictures {
  margin-bottom: 33px;
}

.image-list {
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 130px;
}

.image-list li:not(.image-list li:last-child) {
  margin-right: 8px;
  height: 100%;
}

.store-image-container {
  width: 24%;
}

.store-image {
  height: 100%;
}

.middle {
  margin: 30px 0;
  width: 100%;
  display: flex;
  align-items: center;
  position: relative;
}

.line {
  border-top: 1px dashed #ddd;
  justify-self: stretch;
  width: 100%;
  height: 1px;
}

.middle p {
  justify-self: flex-end;
  font-family: "Varela Round";
  font-size: 11px;
  line-height: 1.64;
  letter-spacing: 0.04px;
  color: #999999;
  position: absolute;
  right: 0;
  background: white;
}
</style>
