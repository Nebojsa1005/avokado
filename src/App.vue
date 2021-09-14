<template>
  <div>
    <app-header :links="links"></app-header>
    <app-location-list></app-location-list>
    <app-soon></app-soon>
    <app-missing-store></app-missing-store>
    <app-image-grid></app-image-grid>
    <app-rewards-and-references></app-rewards-and-references>
    <app-footer :links="links"></app-footer>
  </div>
</template>

<script>
import appHeader from "./components/header.vue";
import appLocationList from "./components/location-list.vue";
import appSoon from "./components/soon.vue";
import appMissingStore from "./components/missingStore.vue";
import appImageGrid from "./components/image-grid.vue";
import appRewardsAndReferences from "./components/rewardsAndReferences.vue";
import appFooter from "./components/footer.vue";
export default {
  components: {
    appHeader,
    appLocationList,
    appSoon,
    appMissingStore,
    appImageGrid,
    appRewardsAndReferences,
    appFooter,
  },
  data() {
    return {
      links: [
        {
          link: "https://slatkoteka.rs/",
          name: "POČETNA",
          text: "Kako funkcionise poriučivanje",
        },
        {
          link: "https://slatkoteka.rs/shop/",
          name: "PORUČIVANJNE",
          text: "Ketering i dostava",
        },
        {
          link: "#lokacije",
          name: "LOKACIJE",
          text: "Seyonske akcije krofni i kronata",
        },
        {
          link: "https://slatkoteka.rs/dostava/",
          name: "DOSTAVA",
          text: "Naručivanje velikih količina",
        },
        {
          link: "#pokloni",
          name: "POKLON",
          text: "kako biramo sastojke za krofne",
        },
        {
          link: "https://slatkoteka.rs/#",
          name: "INFO PULT",
          text: "Još neki korisni link ovde",
        },
      ],
    };
  },
};
</script>


<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
  font-family: "Secular One";
}

.container {
  padding-left: 151px;
  padding-right: 151px;
}

.relative {
  position: relative;
}

ul {
  list-style: none;
}

.link-item {
  text-decoration: none;
  font-size: 18px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.05px;
  color: #000000;
  transition: color 0.2s ease;
}

.link-item:hover {
  color: #f650a0;
}
</style>