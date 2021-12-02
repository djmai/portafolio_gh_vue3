<template>
  <div id="container" class="container">
    <img
      src="https://avatars.githubusercontent.com/u/9259418?v=4"
      alt="Miguel Martínez"
      width="150"
      class="image"
      loading="lazy"
    />
    <h3>MTIE Miguel Martínez</h3>
    <hr />
    <Loading v-if="load" />
    <Card v-else :projects="projects" />
    <!-- <div v-else class="row"> -->
    <!-- <div v-for="project in projects" :key="project.id"> -->
    <!-- </div> -->
    <!-- </div> -->
  </div>
</template>

<script>
import Card from "./Card.vue";
import Loading from "./Loading.vue";

export default {
  name: "Container",
  components: {
    Card,
    Loading,
  },
  data() {
    return {
      projects: [],
      user: null,
      load: false,
    };
  },
  mounted() {
    this.getProjects();
  },
  methods: {
    async getProjects() {
      this.load = true;
      const res = await fetch("https://api.github.com/users/djmai/repos");
      const data = await res.json();
      this.load = false;
      this.projects = data;
      console.log(this.projects);
    },
  },
};
</script>

<style scoped>
/* .cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
} */

#container {
  overflow: hidden;
  /* margin: 1rem; */
  /* padding: 7px; */
  /* border: solid 1px #eee; */
  /* box-shadow: 1px 1px 1px #333; */
  text-align: center;
}

.image {
  border-radius: 50%;
}
</style>
