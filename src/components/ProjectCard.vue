<script>
export default {
    data() {
        return {
        }
    },
    props: {
        title: {
            typeof: String,
            required: true
        },
        author: {
            typeof: String,
            required: true
        },
        image: {
            typeof: String,
            required: true
        }
    }
}
</script>

<template>
    <div class="project-container">
        <div class="project-card">
            <div class="project-image">
                <img src="project-image-url.jpg" alt="Project Image">
            </div>
            <div class="project-details">
                <h2 class="project-title">Project Title</h2>
                <h3 class="project-author">Author: John Doe</h3>
                <p class="project-content">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam at ligula turpis.
                </p>
                <div class="project-category">
                    <span>Category: Web Development</span>
                </div>
                <div class="project-technologies">
                    <h4>Technologies Used:</h4>
                    <ul>
                        <li>HTML</li>
                        <li>CSS</li>
                        <li>JavaScript</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>