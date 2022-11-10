<script>
export default {
    name: 'AppCards',
    props: {
        img: String,
        title: String
    },
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="col">
        <a href="">
            <img :src="img" :alt="title">
            <p>{{ title }}</p>
        </a>
    </div>
</template>

<style lang="scss" scoped>
.col {
    width: calc(100% /6 - 30px);
    margin: 30px 15px;
    max-height: 190px;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }

    p {
        margin-top: 10px;
        color: white;
    }
}
</style>