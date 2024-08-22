<script>
import ProjectCard from './ProjectCard.vue';

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
    <ul>
        <ProjectCard v-for="project in projects">
            {{ project.title }}
        </ProjectCard>
    </ul>
</template>

<style scoped>

</style>