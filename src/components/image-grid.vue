<template>
  <div id="pokloni" class="images-container">
    <div class="images-column column-7 m-l-0">
      <img class="h-549" src="../assets/images/grid-images/img-1.png" />
      <img class="m-b-0 h-193" src="../assets/images/grid-images/img-2.png" />
    </div>

    <div class="images-column column-18">
      <img class="h-178" src="../assets/images/grid-images/img-3.png" />
      <img class="h-270" src="../assets/images/grid-images/img-4.png" />
      <img class="h-270 m-b-0" src="../assets/images/grid-images/img-5.png" />
    </div>

    <div class="images-column column'46">
      <div class="images-row">
        <img class="h-371" src="../assets/images/grid-images/img-6.png" />
        <div class="images-row-column m-l-20">
          <img class="h-178" src="../assets/images/grid-images/img-9.png" />
          <img class="h-178" src="../assets/images/grid-images/img-10.png" />
        </div>
      </div>
      <div class="images-row">
        <div class="images-row-column m-r-20">
          <img class="h-178" src="../assets/images/grid-images/img-7.png" />
          <img class="h-178" src="../assets/images/grid-images/img-9.png" />
        </div>
        <img class="h-371" src="../assets/images/grid-images/img-11.png" />
      </div>
    </div>

    <div class="images-column column-18">
      <img class="h-270" src="../assets/images/grid-images/img-12.png" />
      <img class="h-178" src="../assets/images/grid-images/img-13.png" />
      <img class="m-b-0 h-270" src="../assets/images/grid-images/img-14.png" />
    </div>

    <div class="images-column column-7 m-r-0">
      <img class="m-r-0 h-193" src="../assets/images/grid-images/img-15.png" />
      <img class="m-r-0 h-549" src="../assets/images/grid-images/img-16.png" />
    </div>
  </div>
</template>


<style scope>
.images-container {
  display: flex;
  justify-content: space-between;
  max-width: 100%;
  height: 780px;
  margin-top: 80px;
  margin-bottom: 70px;
  overflow: hidden;
}

.images-column {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  margin: 10px;
  overflow: hidden;
}

.column-7 {
  width: 7%;
}

.column-18 {
  width: 20%;
}

.column-46 {
  width: 46%;
}

.images-column img {
  margin-bottom: 20px;
  width: 100%;
}

.images-row {
  display: flex;
  height: 50%;
  min-width: 100%;
  overflow: hidden;
  margin-bottom: 20px;
}

.h-371 {
  height: 371px;
}

.h-270 {
  height: 270px;
}

.h-549 {
  height: 549px;
}

.h-193 {
  height: 193px;
}

.h-178 {
  height: 178px;
}

.m-l-0 {
  margin-left: 0;
}
.m-l-20 {
  margin-left: 20px;
}

.m-r-0 {
  margin-right: 0;
}

.m-r-20 {
  margin-right: 20px;
}

.m-b-0 {
  margin-bottom: 0;
}
</style>