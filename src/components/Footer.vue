import { computed } from 'vue';
<template>
  <div id="footer" class="footer">
    <footer>
      <h5>&copy; Miguel Martínez - {{ year }}</h5>
    </footer>
  </div>
</template>

<script>
export default {
  name: "Footer",
  computed: {
    year() {
      return new Date().getFullYear();
    },
  },
};
</script>

<style scoped>
.footer {
  background-color: #333;
  padding: 1rem;
  text-align: center;
  color: snow;
  margin-bottom: 0;
}
</style>
