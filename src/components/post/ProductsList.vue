<script setup>

</script>

<template>
  <div class="productList">
    <q-card class="productCard">
      <img src="https://d11666ooz6mihj.cloudfront.net/users/60be475ec0984e617adea4b7/file_storage/images/60be476cc0984e617adea526/media/mini_magick20210803-3572853-1d62q2r.jpg">
      <q-card-section>
        <div class="text-h6"> Syrah </div>
        <div class="text-subtitle2">2017 Colorado</div>
        <div class="text-red">$40</div>
      </q-card-section>
    </q-card>

    <q-card class="productCard">
      <img src="https://d11666ooz6mihj.cloudfront.net/users/60be475ec0984e617adea4b7/file_storage/images/60be4769c0984e617adea512/media/mini_magick20210803-3572853-1aehmpk.jpg">
      <q-card-section>
        <div class="text-h6"> Logan </div>
        <div class="text-subtitle2">2016 Colorado</div>
        <div class="text-red">$26</div>
      </q-card-section>
    </q-card>
    <q-card class="productCard">
      <img src="https://d11666ooz6mihj.cloudfront.net/users/60be475ec0984e617adea4b7/file_storage/images/60be4762c0984e617adea4e0/media/mini_magick20210803-3572853-1vin6r0.jpg">
      <q-card-section>
        <div class="text-h6"> Megan </div>
        <div class="text-subtitle2">2020 Colorado</div>
        <div class="text-red">$2</div>
      </q-card-section>
    </q-card>
    <q-card class="productCard">
      <img src="https://d11666ooz6mihj.cloudfront.net/users/60be475ec0984e617adea4b7/file_storage/images/60be476cc0984e617adea526/media/mini_magick20210803-3572853-1d62q2r.jpg">
      <q-card-section>
        <div class="text-h6"> Syrah </div>
        <div class="text-subtitle2">2017 Colorado</div>
        <div class="text-red">$40</div>
      </q-card-section>
    </q-card>
  </div>
</template>

<style lang="scss">
  .productList {
    display: flex;
    overflow: auto;
    width: auto;
  }
  .productCard {
    width: 180px;
    min-width: 180px;
    height: 320px;
    margin: 10px;

    img {
      height: 200px;
      object-fit: cover;
    }
  }
</style>
