<script>
import axios from 'axios';
import ProjectCard from '@/components/ProjectCard.vue';

export default {
    data() {
        return {
            project: {}
        }
    },
    components: {
        ProjectCard
    }
}
</script>

<template>
    <ProjectCard :author="project.author" :image="project.image" :title="project.title" :content="project.content" :category="project.category.name" :technologies="project.tecnologies" />
</template>

<style scoped>

</style>