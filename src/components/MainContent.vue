<template>

    <main id="album">
        <section class="container">

            <selectMenu :generi="albumGenere" :artisti="artisti"
            @change="setGenere"
            @artistchange="setArtist"/>

            <div class="album-grid">

                <albumCard class="album-card"
                v-for="(album, i) in albumGenereFilter" :key="i" 
                :album="album"/>

            </div>

        </section>
    </main>

</template>

<script>

import albumCard from '../components/AlbumCard.vue';
import selectMenu from '../components/selectMenu.vue';
import axios from 'axios';

export default {
    name: 'mainContent',
    components: {
        albumCard,
        selectMenu,
    },

    data() {
        return {
            albums: [],
            albumGenere: [],
            artisti: [],
            musicGen: '',
            artista: '',
        };
    },

    methods: {
        
        albumCall: function() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then(resp => {
                (console.log(resp.data.response));
                this.albums = resp.data.response;
                this.albumType(resp.data.response);
                this.albumArtist(resp.data.response);
            });
        },

        albumType: function(item) {

            item.forEach((element) => {

                const genere = element.genre;
                if(!this.albumGenere.includes(genere)){
                    this.albumGenere.push(genere);
                }
            });
        },

        albumArtist: function(artisti) {

            artisti.forEach((element) => {

                const artista = element.author;
                this.artisti.push(artista);

            })
        },

        setGenere: function(genere) {

            this.musicGen = genere;
        },

        setArtist: function(artista) {

            this.artista = artista;
        }
    },

    computed: {

        albumGenereFilter: function() {

            return this.albums.filter(album => {
                return album.genre.toLowerCase().includes(this.musicGen.toLowerCase()) && 
                album.author.toLowerCase().includes(this.artista.toLowerCase());
            })
        }
    },
    
    created() {

        this.albumCall();
    },
}

</script>

<style lang="scss" scoped>

@import "../assets/scss/variabili.scss";

#album {
    background-color: $color;
    height: 100vh; 
    overflow-x: hidden;
    overflow-y: scroll;

    .container {
        padding: 150px 10px;

        .album-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 20px 40px;
        }

        .album-card {
            width: calc(100% / 5 - 40px);
            flex-grow: 1;
        }
    }
}
    
</style>