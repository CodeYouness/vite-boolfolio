<script>
import ProjectCard from './ProjectCard.vue';
import axios from 'axios';

export default {
    components: {
        ProjectCard
    },
    data() {
        return {
            projects: [],
        }
    },
    methods:{
        getProjects(){
            axios.get('http://127.0.0.1:8000/api/projects', {
                params: {

                }
            })
            .then((response) => {
                console.log(response.data.results.data);
                this.projects = response.data.results.data;
            })
            .catch((error) => {
                console.log(error)
            });
        }
    },
    created(){
        this.getProjects();
    }
}
</script>

<template>
    <RouterLink v-for="project in projects" :to="{ name: 'Single-project' , params: {id: project.id }}">
        <ProjectCard  :author="project.author" :image="project.image" :title="project.title" :content="project.content" :category="project.category.name" :technologies="project.tecnologies" />
    </RouterLink>
</template>

<style scoped>

</style>