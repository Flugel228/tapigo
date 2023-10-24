<script setup lang="ts">
interface IPost {
  "title": string,
  "description": string,
  "image": string,
}

defineProps<{
  post: IPost
}>();
</script>

<template>
  <div class="col-xl-6 w-100 d-flex justify-content-center align-items-center mb-4">
    <div class="card w-25">
      <div class="card-header d-flex flex-column justify-content-center align-items-center">
        <h2>{{ post.title }}</h2>
      </div>
      <div class="card-body d-flex flex-column justify-content-center align-items-center">
        <img class="w-50" :src="post.image" alt="">
      </div>
      <div class="card-footer d-flex flex-column justify-content-center align-items-center">
        <p>{{ post.description}}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>