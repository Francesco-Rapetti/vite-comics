<script>
// import images from '../assets/img';
export default {
    data() {
        return {
            links: [
                {
                    img: 'buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS'
                }, {
                    img: 'buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE'
                }, {
                    img: 'buy-comics-subscriptions.png',
                    text: 'SUBSCRIPTION'
                }, {
                    img: 'buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR'
                }, {
                    img: 'buy-dc-power-visa.svg',
                    text: 'DC POWER VISA'
                }
            ]
        }
    },

    methods: {
        /**
         * Generates the path of an image based on the provided image name.
         *
         * @param {string} img - The name of the image.
         * @return {string} The path of the image.
         */
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <!-- Quick Links Component -->
    <div id="quick-links" class="w-100 d-flex justify-content-center align-items-center">
        <div class="wrapper d-flex align-items-center justify-content-center flex-wrap w-100">
            <!-- Loop through the links -->
            <a class="d-flex align-items-center" href="#" v-for="link in links">
                <div>
                    <!-- Display the image -->
                    <img class="w-100" :src="getImagePath(link.img)" :alt="link.img">
                </div>
                <!-- Display the link text -->
                <span class="ms-3">{{ link.text }}</span>
            </a>
        </div>
    </div>
</template>

<style scoped>
/* Styling the container */
#quick-links {
    background-color: #1881f3;
}

/* Styling the wrapper */
.wrapper {
    gap: 100px;
    row-gap: 50px;
    padding: 50px 0;
}

/* Styling the images */
img {
    max-height: 60px !important;
    max-width: 60px !important;
}

/* Styling the links */
a {
    text-decoration: none;
    color: white;
}
</style>