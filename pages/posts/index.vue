<script setup lang="ts">
import {useAsyncData} from "nuxt/app";

definePageMeta({
  layout: 'default'
})

const url = 'https://fakestoreapi.com/products?limit=10';

const {data: posts}  = await useAsyncData('posts', () => $fetch(url));
</script>

<template>
  <div class="row mt-5">
    <PostsIndexThePostCard
        v-for="(post, id) of posts"
        :key="id"
        :post="post"
    />
  </div>
</template>

<style scoped>

</style>