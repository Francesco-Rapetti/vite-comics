<script>
export default {
    data() {
        return {
            navbarLinks: [
                {
                    name: 'CHARACTERS',
                    link: '#',
                }, {
                    name: 'COMICS',
                    link: '#',
                }, {
                    name: 'MOVIES',
                    link: '#',
                }, {
                    name: 'TV',
                    link: '#',
                }, {
                    name: 'GAMES',
                    link: '#',
                }, {
                    name: 'COLLECTIBLES',
                    link: '#',
                }, {
                    name: 'VIDEOS',
                    link: '#',
                }, {
                    name: 'FANS',
                    link: '#',
                }, {
                    name: 'NEWS',
                    link: '#',
                }, {
                    name: 'SHOP',
                    link: '#',
                }
            ],
            activeLink: null
        }
    },

    methods: {

    }
}
</script>

<template>
    <div id="navbar-wrapper" class="w-100 bg-white px-3">
        <nav class="navbar navbar-expand-lg w-100 mx-auto py-0 d-flex justify-content-between">
            <a href="#" class="navbar-brand py-3">
                <img src="../assets/img/dc-logo.png" alt="DC logo">
            </a>

            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <div class="w-100"></div>
                <ul class="navbar-nav mb-2 mb-lg-0 justify-self-end">
                    <li v-for="link, i in navbarLinks" class="nav-item fw-bold">
                        <a :class="{ 'active': i === activeLink }" aria-current="page" href="#" @click="activeLink = i">{{
                            link.name }}</a>
                    </li>
                </ul>
            </div>
        </nav>
    </div>
</template>

<style scoped>
nav {
    max-width: 1400px;
    display: flex !important;
    justify-content: space-between !important;
}

ul {
    gap: 30px !important;
    height: 100% !important;
}

li a {
    color: #484c51;
    text-decoration: none;
    border-bottom: 6px solid transparent;
}

li a:hover {
    color: #0c7cec;
}

li a.active {
    color: #0c7cec;
    border-color: transparent;
}


@media screen and (min-width: 992px) {
    li a {
        padding-top: 58px;
        padding-bottom: 52px;
    }

    li a:hover {
        color: #0c7cec;
        border-color: #0c7cec;
    }

    li a.active {
        color: #0c7cec;
        border-color: #0c7cec;
    }
}
</style>
