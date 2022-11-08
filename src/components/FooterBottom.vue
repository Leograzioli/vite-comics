<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="footer-bottom">
        <div class="container flex">
            <div class="ct-left flex">
                <a href="">SIGN-UP NOW!</a>
            </div>

            <div class="ct-right flex">
                <h3>FOLLOW US</h3>
                <a href="">
                    <img src="../assets/img/footer-facebook.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/img/footer-twitter.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/img/footer-youtube.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/img/footer-pinterest.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/img/footer-periscope.png" alt="">
                </a>

            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.footer-bottom {
    display: flex;
    align-items: center;
    padding: 2.5rem;
    background-color: #303030;


    .container {

        .ct-left {
            width: 50%;

            a {
                color: white;
                border: 2px solid $primary-color;
                padding: 0.7rem 0.7rem;
            }
        }

        .ct-right {
            width: 50%;
            justify-content: end;
            align-items: center;
            column-gap: 1rem;

            h3 {
                color: $primary-color;
            }
        }

    }
}
</style>