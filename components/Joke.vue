<template>
  <nuxt-link :to="'jokes/' + id">
    <div class="jokes">
      <p>{{ joke }}</p>
    </div></nuxt-link>
</template>

<script>
export default {
  name: "Joke",
  props: ["joke", "id"],
};
</script>
<style>
.jokes {
  padding: 1rem;
  margin: 1rem 0;
  border: 1px solid #e0eafe;
  border-radius: 15px;
  color: #555;
}
</style>
