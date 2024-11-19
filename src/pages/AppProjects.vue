<script>
import ProjectList from '../components/ProjectList.vue';

export default {
    name: "AppProjects",
    data() {
        return {

        }
    },
    components: {
        ProjectList,
    }
}
</script>

<template>

    <div class="container">
        <div class="row">
            <div class="col-12">
                <h1 class="fw-bold text-center py-4">PROGETTI</h1>
            </div>

            <ProjectList />
        </div>
    </div>
</template>

<style scoped></style>