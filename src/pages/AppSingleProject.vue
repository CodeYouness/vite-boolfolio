<script>
import axios from 'axios';
import ProjectCard from '../components/ProjectCard.vue';

export default {
    data() {
        return {
            project: null
        }
    },
    methods:{
        getProjects(id){
            axios.get(`http://127.0.0.1:8000/api/projects${id}`, {
                params: {

                }
            })
            .then((response) => {
                console.log(response.data.results);
                this.project = response.data.results;
            })
            .catch((error) => {
                console.log(error)
            });
        }
    },
    created(){
        this.getProjects(this.$route.params.id);
    },
    components: {
        ProjectCard
    }
}
</script>

<template>
    <ProjectCard v-if="project != null" :author="project.author" :image="project.image" :title="project.title" :content="project.content" :category="project.category.name" :technologies="project.tecnologies" />
</template>

<style scoped>

</style>