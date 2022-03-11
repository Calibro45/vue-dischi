<template>

    <div class="select-menu">

        <select name="album-type" class="filtro-album" 
        v-model="genSelected" 
        @change="$emit('change', genSelected)">
            <option value="" selected>Home Album</option>
            <option :value="genere" 
            v-for="(genere, i) in generi" :key="i">
                {{ genere }}
            </option>
        </select>

        <select name="artist" class="filtro-album"
        v-model="artistSelected"
        @change="$emit('artistchange', artistSelected)">
            <option value="" selected>Home Album</option>
            <option :value="artista"
            v-for="(artista, i) in artisti" :key="i">
                {{ artista }}
            </option>
        </select>

    </div>

</template>

<script>
export default {

    name: 'selectMenu',

    props: {
        generi: {
            type: Array,
            require: true,
        },
        artisti: {
            type: Array,
            require: true,
        }
    },

    data() {
        return {
            genSelected: '',
            artistSelected: '',
        }
    }
    
}
</script>

<style lang="scss" scoped>

@import "../assets/scss/mixins.scss";

.select-menu {
    margin-bottom: 50px;
    text-align: center;

    .filtro-album {
        @include selectGenere;
        margin-right: 25px;

        &:hover {
            cursor: pointer;
        }
    }
}
    
</style>