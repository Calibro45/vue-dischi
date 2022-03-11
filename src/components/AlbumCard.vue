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
@import "../assets/scss/mixins.scss";

.album-card-wrap {
    @include albumCard;

    .album-logo {
        margin-bottom: 10px;

        img {
            @include albumImg;
        }
    }
    
    .album-title {
        color: #fff;
        @include albumCardTitle;
    }

    .album-info {
        @include albumInfo;
    }
}
    
</style>