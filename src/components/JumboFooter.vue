<script>
export default {
    data() {
        return {
            otherLinks: [
                {
                    title: 'DC COMICS',
                    links: [
                        {
                            name: 'Characters',
                            link: '#'
                        }, {
                            name: 'Comics',
                            link: '#'
                        }, {
                            name: 'Movies',
                            link: '#'
                        }, {
                            name: 'TV',
                            link: '#'
                        }, {
                            name: 'Games',
                            link: '#'
                        }, {
                            name: 'Videos',
                            link: '#'
                        }, {
                            name: 'News',
                            link: '#'
                        }
                    ]
                }, {
                    title: 'SHOP',
                    links: [
                        {
                            name: 'Shop DC',
                            link: '#'
                        }, {
                            name: 'Shop DC Collectibles',
                            link: '#'
                        }
                    ]
                }, {
                    title: 'DC',
                    links: [
                        {
                            name: 'Terms Of Use',
                            link: '#'
                        }, {
                            name: 'Privacy policy (New)',
                            link: '#'
                        }, {
                            name: 'Ad Choices',
                            link: '#'
                        }, {
                            name: 'Advertising',
                            link: '#'
                        }, {
                            name: 'Jobs',
                            link: '#'
                        }, {
                            name: 'Subscriptions',
                            link: '#'
                        }, {
                            name: 'Talent Workshops',
                            link: '#'
                        }, {
                            name: 'CPSC Certificates',
                            link: '#'
                        }, {
                            name: 'Ratings',
                            link: '#'
                        }, {
                            name: 'Shop Help',
                            link: '#'
                        }, {
                            name: 'Contact Us',
                            link: '#'
                        }
                    ]
                }, {
                    title: 'SITES',
                    links: [
                        {
                            name: 'DC',
                            link: '#'
                        }, {
                            name: 'MAD Magazine',
                            link: '#'
                        }, {
                            name: 'DC Kids',
                            link: '#'
                        }, {
                            name: 'DC Universe',
                            link: '#'
                        }, {
                            name: 'DC Power Visa',
                            link: '#'
                        }
                    ]
                }
            ]
        }
    }
}
</script>

<template>
    <div id="jumbo" class="w-100">
        <div class="wrapper d-flex align-items-center position-relative py-5">
            <div class="text-container h-100">
                <div class="d-flex flex-column flex-wrap h-100">
                    <!-- Iterate over each item in the otherLinks array -->
                    <div v-for="item in otherLinks" class="me-5">
                        <!-- Render the title of the item -->
                        <h4>{{ item.title }}</h4>
                        <ul>
                            <!-- Iterate over each link in the links array of the current item -->
                            <li v-for="link in item.links">
                                <!-- Render the link name and set the href attribute -->
                                <a :href="link.link">{{ link.name }}</a>
                            </li>
                        </ul>
                    </div>

                </div>
            </div>
            <!-- Render the DC logo image -->
            <div id="dc-logo" class="position-absolute">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>
</template>

<style scoped>
/* Set the color of all elements to white */
* {
    color: white;
}

/* Styling for the jumbo element */
#jumbo {
    background-image: url(../assets/img/footer-bg.jpg);
    background-position: center;
    background-size: cover;
    overflow: hidden;
}

/* Styling for the wrapper element */
.wrapper {
    height: 418px;
}

/* Styling for the text container */
.text-container {
    position: relative;
    z-index: 1;
}

/* Styling for the DC logo */
#dc-logo {
    right: 16px;
}

/* Styling for unordered lists */
ul {
    list-style-type: none;
    padding: 0;
}

/* Styling for anchor tags */
a {
    text-decoration: none;
    color: #878787;
}

/* Styling for anchor tags on hover */
a:hover {
    color: white;
}
</style>