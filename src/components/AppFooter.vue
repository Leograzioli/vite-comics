<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            dcComicsData: [
                {
                    name: 'Characters'
                },
                {
                    name: 'Comics'
                },
                {
                    name: 'Moviess'
                },
                {
                    name: 'TV'
                },
                {
                    name: 'Games'
                },
                {
                    name: 'Videos'
                },
                {
                    name: 'News'
                }
            ],
            shopData: [
                {
                    name: 'Shop DC'
                },
                {
                    name: 'Shop DC Collectibles'
                }
            ],
            dcData: [
                {
                    name: 'Terms Of Use'
                },
                {
                    name: 'Privacy policy(New)'
                },
                {
                    name: 'Ad Choices'
                },
                {
                    name: 'Advertising'
                },
                {
                    name: 'Jobs'
                },
                {
                    name: 'Subscription'
                },
                {
                    name: 'Talent Workshops'
                },
                {
                    name: 'CPSC Certificates'
                },
                {
                    name: 'Ratings'
                },
                {
                    name: 'Shop Help'
                },
                {
                    name: 'Contact Us'
                },
            ],
            sites: [
                {
                    name: 'DC'
                },
                {
                    name: 'MAD Magazine'
                },
                {
                    name: 'DC Kids'
                },
                {
                    name: 'DC Universe'
                },
                {
                    name: 'DC Power Visa'
                },
            ]
        }
    }
}
</script>

<template>
    <footer>

        <!-- footer top -->
        <div class="footer-top">
            <div class="container flex">

                <div class="links flex">

                    <!-- col  -->
                    <div class="col">
                        <h3>DC COMICS</h3>
                        <ul>
                            <li v-for="(item, index) in dcComicsData" :key="index">
                                {{ item.name }}
                            </li>

                        </ul>

                        <h3>SHOP</h3>
                        <ul>
                            <li v-for="(item, index) in shopData" :key="index">
                                {{ item.name }}
                            </li>
                        </ul>
                    </div>

                    <!-- col  -->
                    <div class="col">
                        <h3>DC COMICS</h3>
                        <ul>
                            <li v-for="(item, index) in dcData" :key="index">
                                {{ item.name }}
                            </li>
                        </ul>
                    </div>

                    <!-- col  -->
                    <div class="col">
                        <h3>DC COMICS</h3>
                        <ul>
                            <li v-for="(item, index) in sites" :key="index">
                                {{ item.name }}
                            </li>
                        </ul>
                    </div>
                </div>

                <div class="logo-footer">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>

        <!-- footer bottom -->
        <div class="footer-bottom">

            <div class="container">
                ciao
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {

    .footer-top {
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        padding: 2rem 0;
        overflow: hidden;

        .links {
            width: 50%;

            .col {

                margin-right: 2rem;

                h3 {
                    color: white;
                    margin: 1rem 0;
                }

                li {
                    color: gray;
                }
            }

        }

        .logo-footer {
            position: relative;
            width: 50%;

            img {
                position: absolute;
                top: -120px;
            }
        }
    }

    .footer-bottom {
        background-color: #303030;

    }
}
</style>