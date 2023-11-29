<script>
export default {
    name: 'AppCard',
    props: ['title', 'image'],
    methods: {
        /**
         * Generates the image path for the given image file.
         *
         * @param {string} img - The name of the image file.
         * @return {string} The URL of the image file.
         */
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div>
        <div class="square-card">
            <img class="w-100" :src="image" alt="">
        </div>
        <h5 class="mt-3">{{ title }}</h5>
    </div>
</template>

<style scoped>
.square-card {
    width: 200px;
    height: 200px;
    overflow: hidden;
    cursor: pointer;
}

h5 {
    width: 200px;
}
</style>