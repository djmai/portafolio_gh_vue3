<template>
  <header>
    <h1>
      {{ title }}
    </h1>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    title: String,
  },
};
</script>

<style>
h1 {
  background-color: #333;
  padding: 1rem;
  text-align: center;
  color: snow;
}
</style>
