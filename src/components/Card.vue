<template>
  <div class="row">
    <div class="col-md-4" v-for="project in projects" :key="project.id">
      <div class="card mb-4 box-shadow">
        <img
          class="card-img-top"
          data-src="holder.js/100px225?theme=thumb&amp;bg=55595c&amp;fg=eceeef&amp;text=Thumbnail"
          alt="Thumbnail [100%x225]"
          style="height: 225px; width: 100%; display: block"
          src="data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%22311%22%20height%3D%22225%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%20311%20225%22%20preserveAspectRatio%3D%22none%22%3E%3Cdefs%3E%3Cstyle%20type%3D%22text%2Fcss%22%3E%23holder_17d77ef95e8%20text%20%7B%20fill%3A%23eceeef%3Bfont-weight%3Abold%3Bfont-family%3AArial%2C%20Helvetica%2C%20Open%20Sans%2C%20sans-serif%2C%20monospace%3Bfont-size%3A16pt%20%7D%20%3C%2Fstyle%3E%3C%2Fdefs%3E%3Cg%20id%3D%22holder_17d77ef95e8%22%3E%3Crect%20width%3D%22311%22%20height%3D%22225%22%20fill%3D%22%2355595c%22%3E%3C%2Frect%3E%3Cg%3E%3Ctext%20x%3D%22101.578125%22%20y%3D%22119.7%22%3EThumbnail%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fsvg%3E"
          data-holder-rendered="true"
        />
        <div class="card-header">
          <h6 class="my-0 font-weight-normal">{{ project.name }}</h6>
        </div>
        <div class="card-body">
          <p class="card-text">
            {{
              project.description == null
                ? "Proyecto sin descripción"
                : project.description
            }}
          </p>
          {{ project.homepage }}
          <div class="d-flex justify-content-between align-items-center">
            <div id="buttons" class="btn-group">
              <Button
                color="dark"
                :url="project.html_url"
                nameUrl="GitHub"
                iconUrl="bi bi-github"
              />
              <Button
                color="info"
                :url="project.hompage"
                nameUrl="Home Page"
                iconUrl="bi bi-globe"
                v-if="project.homepage != null"
              />
            </div>
            <small class="text-muted">{{ project.owner.login }}</small>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Button from "./Button.vue";
export default {
  components: { Button },
  name: "Card",
  props: {
    project: {
      type: Object,
    },
    projects: {
      type: Object,
    },
  },
};
</script>

<style scoped>
/* .card {
  width: 250px;
  height: 150px;
  margin: 7px;
  border: solid 1px #eee;
  box-shadow: 1px 1px 4px #333;
  text-align: center;
} */
</style>
