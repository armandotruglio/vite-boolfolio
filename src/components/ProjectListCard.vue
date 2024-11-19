<script>
export default {
    name: "ProjectListCard",
    data() {
        return {

        }
    },
    props: {
        projectObject: {
            type: Object,
            required: true,
        }
    },
    computed: {
        projectImage() {
            return "http://127.0.0.1:8000/storage/" + this.projectObject.image;
        }
    }
}
</script>

<template>
    <div class="col-6">
        <div class="card">
            <img :src="projectImage" class="card-img-top" :alt="projectObject.title">
            <div class="card-body">
                <h5 class="card-title">{{ projectObject.title }}</h5>
                <p class="card-text">
                    {{ projectObject.description }}
                </p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
        </div>
    </div>
</template>

<style scoped></style>