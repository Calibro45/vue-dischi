<template>

    <div class="album-card-wrap">
        <figure class="album-logo">
            <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
        </figure>
        
        <div class="album-title">
            <p>Titolo Album</p>
        </div>

        <div class="album-info">
            <p>Artista</p>
            <p>Anno Album</p>
        </div>
    </div>

</template>

<script>

export default {
    name: 'albumCard',
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