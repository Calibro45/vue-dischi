<template>

    <main id="album">
        <div class="container">

            <albumCard />

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
    }
}
    
</style>