<template>

    <div class="album-card-wrap">
        <figure class="album-logo">
            <img :src="album.poster" alt="">
        </figure>
        
        <div class="album-title">
            <p>{{ album.author }}</p>
        </div>

        <div class="album-info">
            <p>{{ album.title }}</p>
            <p>{{ album.year }}</p>
        </div>
    </div>

</template>

<script>

export default {
    name: 'albumCard',

    props: {
        album: {
            type: Object,
            require: true,
        }
    },
}

</script>

<style lang="scss" scoped>
@import "../assets/scss/variabili.scss";

.album-card-wrap {
    padding: 20px;
    background-color: $colorsec;
    text-align: center;

    .album-logo {
        margin-bottom: 10px;

        img {
            aspect-ratio: 1;
            object-fit: cover;
            object-position: center;
        }
    }
    
    .album-title {
        color: #fff;
        text-transform: uppercase;
        padding: 10px 15px;
        font-weight: 700;
        font-size: 18px;
        margin-bottom: 20px;
    }

    .album-info {
        font-size: 14px;
        color: $colorText;
        font-weight: 500;
    }
}
    
</style>