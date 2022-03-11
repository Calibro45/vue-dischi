<template>

    <div class="select-menu">
        <select name="album-type" class="filtro-album" v-model="genSelected">
          <option :value="genere" v-for="(genere, i) in generi" :key="i">
              {{ genere }}
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
        }
    },

    data() {
        return {
            genSelected: '',
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

        &:hover {
            cursor: pointer;
        }
    }
}
    
</style>