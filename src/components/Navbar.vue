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
        /**
         * Scroll function that resize the navbar based on scroll position.
         *
         * @return {void} This function doesn't return anything.
         */
        scrollFunction() {
            // Get the navbar element by its ID
            const navbar = document.getElementById("navbar-wrapper");
            // Get the logo element by its ID
            const logo = document.getElementById("logo");
            // Get all the anchor elements inside list items
            const links = document.querySelectorAll("li a");

            // Check if the page has been scrolled down more than 50 pixels
            if (document.body.scrollTop > 50 || document.documentElement.scrollTop > 50) {
                console.log("scrolled");

                // Add a shadow class to the navbar for a visual effect
                navbar.classList.add("shadow");
                // Reduce the width of the logo
                logo.style.width = "50px";
                // Adjust the padding of each link for better alignment
                links.forEach((link) => {
                    link.style.paddingBottom = "27px";
                });
            } else {
                console.log("not scrolled");

                // Remove the shadow class from the navbar
                navbar.classList.remove("shadow");
                // Restore the original width of the logo
                logo.style.width = "103px";
                // Restore the original padding of each link
                links.forEach((link) => {
                    link.style.paddingBottom = "53px";
                });
            }
        }
    },

    mounted() {
        window.onscroll = () => {
            this.scrollFunction();
        }
    }
}

</script>

<template>
    <!-- Wrapper for the navbar -->
    <div id="navbar-wrapper" class="w-100 bg-white px-3 position-fixed">
        <!-- Navbar -->
        <nav class="navbar navbar-expand-lg w-100 mx-auto py-0 d-flex justify-content-between">
            <!-- Navbar Brand -->
            <a href="#" class="navbar-brand py-3">
                <img id="logo" src="../assets/img/dc-logo.png" alt="DC logo">
            </a>

            <!-- Navbar Toggler -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <!-- Navbar Collapse -->
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <!-- Spacer -->
                <div class="w-100"></div>

                <!-- Navbar Links -->
                <ul class="navbar-nav mb-2 mb-lg-0 justify-self-end">
                    <!-- Loop through navbarLinks array -->
                    <li v-for="link, i in navbarLinks" class="nav-item fw-bold">
                        <!-- Individual Navbar Link -->
                        <a :class="{ 'active': i === activeLink }" aria-current="page" href="#" @click="activeLink = i">{{
                            link.name }}</a>
                    </li>
                </ul>
            </div>
        </nav>
    </div>
    <div id="navbar-spacer"></div>
</template>

<style scoped>
/* CSS for the navbar wrapper */
#navbar-wrapper {
    position: relative;
    z-index: 99;
    transition: all 0.3s ease-in-out;
}

/* Spacer height for the navbar */
#navbar-spacer {
    height: 135px;
}

/* CSS for images with transition and width */
img {
    transition: all 0.3s ease-in-out;
    width: 103px;
}

/* Styles for the navigation bar */
nav {
    max-width: 1400px;
    display: flex !important;
    justify-content: space-between !important;
}

/* Styles for the unordered list */
ul {
    gap: 30px !important;
    height: 100% !important;
}

li {
    height: 1.3em;
    overflow: hidden;
}

/* Styles for the links in the list items */
li a {
    color: #484c51;
    text-decoration: none;
    border-bottom: 6px solid transparent;
    transition: all 0.3s ease-in-out;
}

/* Styles for the links when hovered */
li a:hover {
    color: #0c7cec;
}

/* Styles for the active link */
li a.active {
    color: #0c7cec;
    border-color: transparent;
}

/* Media query for screens larger than 992px */
@media screen and (min-width: 992px) {

    li {
        height: auto;
        overflow: visible;
    }

    /* Additional styles for the links in the media query */
    li a {
        padding-top: 58px;
        padding-bottom: 53px;
    }

    /* Additional styles for the links when hovered in the media query */
    li a:hover {
        color: #0c7cec;
    }

    /* Additional styles for the active link in the media query */
    li a.active {
        color: #0c7cec;
        border-color: #0c7cec;
    }
}
</style>
