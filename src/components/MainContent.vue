<template>

    <main id="album">
        <div class="container">

            <albumCard class="album-card"
            v-for="(album, i) in albums" :key="i" />

        </div>
    </main>

</template>

<script>
import albumCard from '../components/AlbumCard.vue';
import axios from 'axios';

export default {
    name: 'mainContent',
    components: {
        albumCard,
    },

    data() {
        return {
            albums: [],
        }
    },

    methods: {
        
        albumCall: function() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then(resp => {
                (console.log(resp.data));
                this.albums = resp.data;
            });
        }
    },
    
    created() {

        this.albumCall();
        
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