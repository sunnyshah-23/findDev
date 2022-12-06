<template>
    <div class="project">
        <div v-for="proj in projects" :key="proj.id">
            <ProjectItem :proj="proj" />
        </div>

    </div>



</template>'

<script>

import ProjectItem from './ProjectItem.vue'


export default {
    name: 'ProjectCard',
    components: {
        ProjectItem
    },
    props: {

        projects: Array
    }
}

</script>

<style scoped>
.project {
    grid-area: project;
}
</style>