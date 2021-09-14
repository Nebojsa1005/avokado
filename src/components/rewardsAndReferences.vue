<template>
  <div class="wrapper">
    <div class="rewards">
      <div class="reward-logos">
        <h2>NAGREDE</h2>
        <div>
          <img class="logo" src="../assets/images/rewards/logo-2.png" />
          <img class="logo" src="../assets/images/rewards/logo-1.png" />
        </div>
      </div>
      <div class="suported">
        <h2>PORŽALI SMO</h2>
        <div class="square">
          <div class="card"></div>
          <div class="card card-small"></div>
          <div class="card"></div>
          <div class="card"></div>
          <div class="card card-small"></div>
          <div class="card"></div>
          <div class="card"></div>
          <div class="card"></div>
        </div>
      </div>
    </div>
    <div class="reference-and-catering">
      <div class="reference">
        <h2>REFERENCE</h2>
        <div class="square">
          <div class="card normal-card"></div>
          <div class="card md-card"></div>
          <div class="card normal-card"></div>
          <div class="card md-card"></div>
          <div class="card sm-card"></div>
        </div>
      </div>
      <div class="catering">
        <h2>KETERING</h2>
        <p class="catering-text">
          Želite da poručite neke od Slatkoteka proizvoda za vašu proslavu?
        </p>
        <div class="catering-container">
          <span @click="orderCatering">{{
            catering ? "Otkaži ketering" : "Ketering"
          }}</span>
          <p v-if="showOrderMessage" class="catering-order">
            Ketering tim je na Vašoj adresi za {{ minutes }} minuta!
          </p>
          <p class="no-catering" v-if="showCancelOrderMessage">
            Ketering je otkazan!
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      minutes: null,
      catering: false,
      showOrderMessage: false,
      showCancelOrderMessage: false,
    };
  },
  methods: {
    orderCatering() {
      this.catering = !this.catering;
      if (this.catering) {
        this.showCancelOrderMessage = false;
        this.showOrderMessage = true;
        this.minutes = Math.floor(Math.random() * 15);
        setTimeout(() => {
          this.showOrderMessage = false;
        }, 2000);
      }
      if (!this.catering) {
        this.showOrderMessage = false;
        this.showCancelOrderMessage = true;
        setTimeout(() => {
          this.showCancelOrderMessage = false;
        }, 2000);
      }
    },
  },
};
</script>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  width: 100%;
  padding-left: 139px;
  margin-bottom: 41px;
}

.rewards {
  display: flex;
  width: 100%;
  align-items: flex-start;
  margin-bottom: 57px;
}

h2 {
  margin-bottom: 24px;
  font-size: 18px;
  letter-spacing: 0.13px;
}

.reward-logos {
  width: 15%;
  height: 150px;
  margin-right: 50px;
}

.logo {
  width: 80px;
  height: 80px;
  margin-right: 20px;
}

.suported {
  width: 75%;
}

.suported h2 {
  margin-bottom: 45px;
}

.square {
  width: 100%;
  display: flex;
}

.card {
  width: 14%;
  height: 42px;
  margin: 0 12px 0 0;
  background-color: #d8d8d8;
}

.card-small {
  width: 8%;
}

.reference-and-catering {
  width: 100%;
  display: flex;
  justify-content: flex-start;
}

.reference,
.catering {
  min-height: 100%;
  margin-right: 53px;
}

.reference {
  width: 40%;
}

.reference .normal-card {
  width: 25%;
}

.reference .md-card {
  width: 20%;
}

.refenrece .sm-card {
  width: 10%;
  margin-right: 0;
}

.reference h2 {
  margin-bottom: 24px;
}

.catering {
  display: flex;
  flex-direction: column;
}

.catering h2 {
  margin-bottom: 4px;
}

.catering-text {
  margin-bottom: 12px;
  font-family: "Varela Round";
  font-size: 16px;
}

.catering span {
  text-align: center;
  height: 30px;
  min-width: 105px;
  padding: 5px 8px 5px 8px;
  border-radius: 1.9px;
  background-color: #f454a0;
  color: white;
}

.catering-container {
  display: flex;
}

.catering-container span {
  margin-right: 10px;
}

.catering-order,
.no-catering {
  height: 30px;
  color: white;
  padding: 5px 8px 5px 8px;
  margin-bottom: 0;
  transition: all 0.12s ease;
}

.catering-order {
  background: steelblue;
}

.no-catering {
  background: rgb(240, 29, 29);
}
</style>