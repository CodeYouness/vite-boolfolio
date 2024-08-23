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
        },
        content: {
            typeof: String,
            required: true
        },
        category: {
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
                <img src="" alt="Project Image">
            </div>
            <div class="project-details">
                <h2 class="project-title">{{ title }}</h2>
                <h3 class="project-author">Author: {{ author }}</h3>
                <p class="project-content">
                    {{ content }}
                </p>
                <div class="project-category">
                    <span>Category: {{ category }}</span>
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

.project-container {
    display: flex;
    justify-content: center;
    align-items: center;
}

.project-card {
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    width: 80%;
    max-width: 800px;
    display: flex;
    flex-direction: column;
    margin: 20px;

    @media(min-width: 768px) {
        flex-direction: row;
    }
}

.project-image img {
    width: 100%;
    height: auto;

    @media(min-width: 768px) {
        width: 50%;
        height: 100%;
    }
}

.project-details {
    padding: 20px;
    flex: 1;
}

.project-title {
    font-size: 24px;
    margin-bottom: 10px;
    color: #333;
}

.project-author {
    font-size: 18px;
    margin-bottom: 10px;
    color: #666;
}

.project-content {
    font-size: 16px;
    color: #555;
    margin-bottom: 20px;
}

.project-category {
    font-weight: bold;
    color: #ff6347;
    margin-bottom: 20px;
}

.project-technologies h4 {
    margin-bottom: 10px;
    color: #333;
}

.project-technologies ul {
    list-style-type: disc;
    padding-left: 20px;
}

.project-technologies li {
    font-size: 14px;
    color: #666;
}
</style>