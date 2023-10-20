<script setup>
import { ref } from 'vue'
import ProductsList from 'src/components/post/ProductsList.vue'

const slide = ref(0)
const text = ref('')
</script>

<template>
    <q-card class="post my-card">
      <q-item>
        <q-item-section avatar>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label>Elsom Cellars</q-item-label>
          <q-item-label caption>
            Seattle, WA
          </q-item-label>
        </q-item-section>
      </q-item>

      <q-separator />

      <q-carousel
        v-model="slide"
        transition-prev="slide-right"
        transition-next="slide-left"
        swipeable
        animated
        control-color="white"
        navigation
        padding
        arrows
        height="300px"
        class="shadow-1 rounded-borders"
      >
      <q-carousel-slide :name="0">
        <q-video
          class="absolute-full"
          src="https://www.youtube.com/embed/dQw4w9WgXcQ?si=dV1X7RgP0m3uNMlO"
        />
      </q-carousel-slide>
        <q-carousel-slide :name="1" img-src="https://d11666ooz6mihj.cloudfront.net/users/60be475ec0984e617adea4b7/file_storage/images/61c49589c0984e9c62b9720b/media/mini_magick20211223-1088139-1z0x494.jpg" />
        <q-carousel-slide :name="2" img-src="https://d11666ooz6mihj.cloudfront.net/users/60be475ec0984e617adea4b7/file_storage/images/61c49589c0984e9c62b9720a/media/mini_magick20211223-1088139-1j1ass1.jpg" />
        <q-carousel-slide :name="3" img-src="https://d11666ooz6mihj.cloudfront.net/users/60be475ec0984e617adea4b7/file_storage/images/61c49589c0984e9c62b97209/media/mini_magick20211223-1088139-kfj5g3.jpg" />
      </q-carousel>

      <!-- <q-card-section>
        <div class="text-h6">Our Changing Planet</div>
        <div class="text-subtitle2">by John Doe</div>
      </q-card-section> -->

      <q-card-section class="">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
      </q-card-section>

      <q-card-actions align="between">
        <q-btn flat round color="red" icon="favorite"> 2 Likes </q-btn>
        <q-btn flat round color="grey" icon="comment"> 2 comments </q-btn>
        <q-btn flat round color="grey" icon="share"> 2 shares </q-btn>
        <q-btn flat round color="grey" icon="bookmark"> 41 saved </q-btn>
      </q-card-actions>

      <q-separator />

      <products-list />

      <q-separator />

      <q-card-section>
        <q-input bottom-slots v-model="text" label="Comment" counter maxlength="12" :dense="true">
          <template v-slot:before>
            <q-avatar size="36px">
              <img src="https://cdn.quasar.dev/img/avatar5.jpg">
            </q-avatar>
          </template>

          <template v-slot:append>
            <q-icon v-if="text !== ''" name="close" @click="text = ''" class="cursor-pointer" />
            <!-- <q-icon name="schedule" /> -->
          </template>

          <template v-slot:hint>
            Field hint
          </template>

          <template v-slot:after>
            <q-btn round dense flat icon="send" />
          </template>
        </q-input>

      </q-card-section>

    </q-card>
</template>

<style lang="scss">
  .post {
    width: 600px;
    margin-bottom: 20px;
    @media screen and (max-width: 600px) {
      width: calc(100% - 20px);
    }
  }
</style>
