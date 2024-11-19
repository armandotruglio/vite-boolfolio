<script>
import axios from 'axios';
import ProjectListCard from './ProjectListCard.vue';

export default {
    name: "ProjectList",
    data() {
        return {
            apiUrl: "http://127.0.0.1:8000/api/projects",
            projectList: [],
        }
    },
    components: {
        ProjectListCard,
    },
    methods: {
        getProjects() {
            axios.get(this.apiUrl)
                .then((response) => {
                    console.log(response.data.results);
                    this.projectList = response.data.results;
                })
                .catch(function (error) {
                    console.log(error);
                });
        }
    },
    created() {
        this.getProjects();
    }
}
</script>

<template>
    <div class="row g-4">
        <ProjectListCard v-for="project in projectList" :key="project.id" :projectObject="project" />
    </div>
</template>

<style scoped></style>