<script setup>
import PostItem from 'src/components/post/PostItem.vue'
</script>

<template>
  <div class="postList">
    <post-item
    v-for="i in 3" :key="i" />
  </div>
</template>

<style lang="scss">
  .postList {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 20px;
  }
</style>
