<template>
  <div class="box1">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: "GoodbyeWorld",
  props: {
    msg: String
  }
};
</script>

<style scoped>
.box1 {
  border: 5px solid deeppink;
  padding: 2rem;
  background-color: antiquewhite;
}
h1 {
  color: deeppink;
}
</style>

