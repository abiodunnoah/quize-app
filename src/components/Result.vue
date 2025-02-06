<script setup>
import { defineProps } from "vue";
import { RouterLink } from "vue-router";

const { numberOfCorrectAnswers, quizQuestionLength } = defineProps([
  "quizQuestionLength",
  "numberOfCorrectAnswers",
]);
</script>

<template>
  <div class="results">
    <p>Your results...</p>
    <h1>{{ numberOfCorrectAnswers }}/{{ quizQuestionLength }}</h1>
    <RouterLink to="/">Go back</RouterLink>
  </div>
</template>

<style scope>
.results {
  text-align: center;
  padding: 100px 0;
}

p {
  font-size: 25px;
}

h1 {
  font-size: 80px;
}
</style>
