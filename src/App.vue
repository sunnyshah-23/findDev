<template>
  <div class="container">
    <HeaderTop />

    <Project :projects="projects" />
  </div>

</template>
<script>

import HeaderTop from "./components/Header.vue"
import Project from "./components/Project.vue"


export default {
  name: 'App',
  components: {
    HeaderTop,
    Project

  },
  data() {
    return {
      projects: [],

    }
  },

  methods: {
    // promises

    async fetchProject() {
      const res = await fetch('https://rich-gold-gecko-kit.cyclic.app/api')
      const data = await res.json()
      return data
    }


  },
  async created() {
    this.projects = await this.fetchProject()
  }
}

</script>
<style >
.container {
  display: grid;
  grid-template-rows: 0.05fr 1fr;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas:
    "nav nav nav"
    "project project project"

  ;
}
</style>