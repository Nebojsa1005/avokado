<template>
  <div class="wrapper">
    <img src="../assets/images/curvy-line.svg" class="curvy-image" />
    <h1>NEDOSTAJE SLATKOTEKA U VAŠEM GRADU?</h1>
    <p>
      Saznajte više o Slatkoteka franšizi
      <a href="https://slatkoteka.rs/o-nama/">ovde</a>.
    </p>
  </div>
</template>

<style scoped>
.wrapper {
  height: 372px;
  width: 100%;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.curvy-image {
  width: 100%;
  top: 0;
  left: 0;
  position: absolute;
  z-index: -1;
}

h1 {
  margin-bottom: 24px;
  font-size: 35px;
  letter-spacing: 0.12px;
  color: #000000;
}

p,
p a {
  text-decoration: none;
  font-family: "Varela Round";
  margin-top: 24px;
  font-size: 16px;
  line-height: 1.13;
  letter-spacing: 0.05px;
  color: #666666;
  transition: color 0.2s ease;
}

a {
  cursor: pointer;
}

a:hover {
  color: #f650a0;
}
</style>