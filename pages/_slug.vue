<template>
  <div class="container">
    <div>
      <h1>There should be a title here: {{ myData.title }}</h1>
      <p>There should be some text below:
        <br>
        {{ myData.text }}
      </p>
      <client-only>
        <nuxt-link to="/fr/test">Go to nested slug</nuxt-link>
      </client-only>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return { myData: { title: "", text: "" } };
  },
  fetch() {
    this.myData.title = "Fetched a title!";
    this.myData.text = "Fetch a text!";
  }
};
</script>

<style scoped>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
h1 {
  font-weight: 400;
}
.name {
  color: #00C48D;
}
p {
  margin-top: 20px;
}
</style>
