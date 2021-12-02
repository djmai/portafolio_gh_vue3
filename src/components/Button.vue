<template>
  <!-- <div id="buttons" class="btn-group"> -->
  <a :href="url" type="button" :class="setColor" target="_blank" :alt="nameUrl">
    <i v-if="iconUrl" :class="iconUrl"></i>
    <span v-else>{{ nameUrl }}</span>
  </a>
  <!-- <button type="button" class="btn btn-sm btn-outline-secondary">Edit</button> -->
  <!-- </div> -->
</template>

<script>
export default {
  name: "Button",
  props: {
    color: String,
    url: String,
    nameUrl: String,
    iconUrl: String,
  },
  computed: {
    setColor() {
      return this.color == ""
        ? `btn btn-sm btn-primary`
        : `btn btn-sm btn-${this.color}`;
    },
    setUrl() {
      return this.url == "" ? `#` : `${this.url}`;
    },
    setName() {
      // return this.iconUrl != "" ? `<i class="${this.iconUrl}"></i>` : `${this.url}`;
      return this.iconUrl != ""
        ? `<i class="${this.iconUrl}"></i>`
        : this.nameUrl != ""
        ? `${this.nameUrl}`
        : `Agregar un nombre al icono`;
    },
  },
};
</script>

<style></style>
