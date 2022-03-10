<template>

    <main id="album">
        <div class="container">

            <albumCard class="album-card"/>

        </div>
    </main>

</template>

<script>
import albumCard from '../components/AlbumCard.vue';

export default {
    name: 'mainContent',
    components: {
        albumCard,
    }
    
}
</script>

<style lang="scss" scoped>

@import "../assets/scss/variabili.scss";

#album {
    background-color: $color;
    height: calc(100vh - 76px); 

    .container {
        padding: 70px 10px;
        display: flex;
        flex-wrap: wrap;

        .album-card {
            width: calc(100% / 5);
        }
    }
}
    
</style>