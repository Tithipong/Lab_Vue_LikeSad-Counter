<template>
  <div class="col-md-4">
    <div class="card shadow-sm">
      <img
        src="https://templated.co/meme-templates/wp-content/uploads/cat-meme-template-2.jpg"
        class="card-img-top"
        alt="Meme Image"
        style="width: 100%; height: 400px; object-fit: cover"
      />
      <div class="card-body">
        <p class="card-text">El Gato: Mew.</p>
        <div class="d-flex justify-content-between align-items-center">
          <div>
            <button
              type="button"
              class="btn btn-outline-primary"
              @click="likeClick()"
            >
            <i class="bi bi-hand-thumbs-up-fill"></i>Like {{ like }}
            </button>
          </div>
          <button
            type="button"
            class="btn btn-outline-danger"
            @click="sadClick()"
          >
            <i class="bi bi-emoji-frown-fill"></i> Sad {{ sad }}
          </button>
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
