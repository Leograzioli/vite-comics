<script>
import FooterBottom from './FooterBottom.vue';

export default {
    name: 'AppFooter',
    data() {
        return {
            dcComicsData: [
                {
                    name: 'Characters',
                    href: '/Characters'
                },
                {
                    name: 'Comics',
                    href: '/Comics'
                },
                {
                    name: 'Moviess',
                    href: '/Moviess'
                },
                {
                    name: 'TV',
                    href: '/TV'
                },
                {
                    name: 'Games',
                    href: '/Games'
                },
                {
                    name: 'Videos',
                    href: '/Videos'
                },
                {
                    name: 'News',
                    href: '/News'
                }
            ],
            shopData: [
                {
                    name: 'Shop DC',
                    href: '/Shop-DC'
                },
                {
                    name: 'Shop DC Collectibles',
                    href: '/Shop-DC-Collectibles'
                }
            ],
            dcData: [
                {
                    name: 'Terms Of Use',
                    href: '/Terms-Of-Use'
                },
                {
                    name: 'Privacy policy(New)',
                    href: '/Privacy-policy'
                },
                {
                    name: 'Ad Choices',
                    href: '/ad-choise'
                },
                {
                    name: 'Advertising',
                    href: '/advertising'
                },
                {
                    name: 'Jobs',
                    href: '/jobs'
                },
                {
                    name: 'Subscription',
                    href: '/subscription'
                },
                {
                    name: 'Talent Workshops',
                    href: '/talent-workshops'
                },
                {
                    name: 'CPSC Certificates',
                    href: '/cpsc-certificates'
                },
                {
                    name: 'Ratings',
                    href: '/ratings'
                },
                {
                    name: 'Shop Help',
                    href: '/shop-help'
                },
                {
                    name: 'Contact Us',
                    href: '/contact-us'
                },
            ],
            sites: [
                {
                    name: 'DC',
                    href: '/DC'
                },
                {
                    name: 'MAD Magazine',
                    href: '/MAD-Magazine'
                },
                {
                    name: 'DC Kids',
                    href: '/DC-Kids'
                },
                {
                    name: 'DC Universe',
                    href: '/DC-Universe'
                },
                {
                    name: 'DC Power Visa',
                    href: '/power-visa'
                },
            ]
        }
    },
    components: {
        FooterBottom
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
                                <a :href="item.href">{{ item.name }}</a>
                            </li>

                        </ul>

                        <h3>SHOP</h3>
                        <ul>
                            <li v-for="(item, index) in shopData" :key="index">
                                <a :href="item.href">{{ item.name }}</a>
                            </li>
                        </ul>
                    </div>

                    <!-- col  -->
                    <div class="col">
                        <h3>DC COMICS</h3>
                        <ul>
                            <li v-for="(item, index) in dcData" :key="index">
                                <a :href="item.href">{{ item.name }}</a>
                            </li>
                        </ul>
                    </div>

                    <!-- col  -->
                    <div class="col">
                        <h3>DC COMICS</h3>
                        <ul>
                            <li v-for="(item, index) in sites" :key="index">
                                <a :href="item.href">{{ item.name }}</a>
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
            <FooterBottom />
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

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
                    color: $secondary-color;
                    line-height: 1.5rem;
                }
            }
        }

        .logo-footer {
            position: relative;
            width: 50%;

            img {
                position: absolute;
                top: -10px;
            }
        }
    }
}
</style>