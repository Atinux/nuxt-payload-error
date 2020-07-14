<template>
  <div class="container">
    <div>
      <h1>There should be a title here: {{ myData.title }}</h1>
      <p>There should be some text below:
        <br>
        {{ myData.text }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return { myData: { title: "", text: "" } };
  },
  fetch() {
    this.myData.title = "Nested - Dynamic subpage!";
    this.myData.text = "Nested - subpage text!";
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
