<script>
export default {
    data() {
        return {
            socials: [
                {
                    img: 'footer-facebook.png',
                    link: '#'
                }, {
                    img: 'footer-twitter.png',
                    link: '#'
                }, {
                    img: 'footer-youtube.png',
                    link: '#'
                }, {
                    img: 'footer-pinterest.png',
                    link: '#'
                }, {
                    img: 'footer-periscope.png',
                    link: '#'
                }
            ]
        }
    },

    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div id="footer">
        <div class="wrapper d-flex justify-content-between align-items-center py-4">
            <button>SIGN-UP NOW!</button>
            <div id="social" class="d-flex align-items-center">
                <h5 class="m-0">FOLLOW US</h5>
                <a v-for="social in socials" :href="social.link">
                    <img :src="getImagePath(social.img)" :alt="social.img">
                </a>
            </div>
        </div>
    </div>
</template>

<style scoped>
#footer {
    background-color: #333333;
}

button {
    color: white;
    background-color: transparent;
    border: 2px solid #0282F9;
    padding: 10px 20px;
    font-weight: 600;
}

button:hover {
    background-color: #0282F9;
}

#social {
    gap: 20px;
    color: #0282F9;
}
</style>