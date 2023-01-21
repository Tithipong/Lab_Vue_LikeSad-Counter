<template>
  <div class="col-md-4">
    <div class="card shadow-sm">
      <svg
        class="bd-placeholder-img card-img-top"
        width="100%"
        height="225"
        xmlns="http://www.w3.org/2000/svg"
        role="img"
        aria-label="Placeholder: Thumbnail"
        preserveAspectRatio="xMidYMid slice"
        focusable="false"
      >
        <title>Placeholder</title>
        <rect width="100%" height="100%" fill="#55595c" />
        <text x="50%" y="50%" fill="#eceeef" dy=".3em">Thumbnail</text>
      </svg>
      <div class="card-body">
        <p class="card-text">
          This is a wider card with supporting text below as a natural lead-in
          to additional content. This content is a little bit longer.
        </p>
        <div class="d-flex justify-content-between align-items-center">
          <div>
            <button
              type="button"
              class="btn btn-outline-primary"
              @click="likeClick()"
            >
              <i class="bi bi-hand-thumbs-up-fill"></i> Like {{ like }}
            </button>
            <button
              type="button"
              class="btn btn-outline-primary"
              @click="sadClick()"
            >
              <i class="bi bi-emoji-frown-fill"></i> Sad {{ sad }}
            </button>
          </div>
          <small class="text-muted">9 mins</small>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const like = ref(0);
const sad = ref(0);
function likeClick() {
  like.value++;
}
function sadClick() {
  sad.value++;
}
</script>

<style scoped>
h1 {
  color: rgb(206, 134, 0);
}

h2 {
  color: rgb(255, 114, 222);
}

h3 {
  color: rgb(9, 141, 0);
}
</style>
