<template>
  <form class="form" @submit.prevent="onSubmit">
    <input
      class="search"
      type="text"
      v-model="text"
      placeholder="Search Jokes..."
    />
    <input class="submit" type="submit" value="Search Jokes" />
  </form>
</template>

<script>
export default {
  name: "SearchJokes",
  data() {
    return {
      text: "",
    };
  },
  methods: {
    onSubmit() {
      this.$emit("search-text", this.text);
      this.text = "";
    },
  },
};
</script>

<style>
.form {
  margin: 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0;
  
}

.form .search {
  width: 100%;
  height: 50px;
  line-height: 70px;
  padding: 10px 16px;
  border-radius: 45px;
  border: 1px solid #4178e6;
  font-family: Poppins;

}
.form .submit {
  background: #4178e6;
  color: #fff;
  height: 50px;
  border: none;
  width: 24%;
  border-radius: 45px;
  font-family: Poppins;
  margin-left: -45px;
}
</style>