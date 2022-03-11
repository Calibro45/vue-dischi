<template>

    <header>
        <figure class="logo">
            <img src="../assets/img/spoty.png" alt="">
        </figure>
    </header>

</template>

<script>

export default {
    name: 'mainHeader',
    
}

</script>

<style lang="scss" scoped>
@import "../assets/scss/mixins.scss";
@import "../assets/scss/variabili.scss";

header {
    @include navBar;

    .logo {
        width: 46px;
        height: 46px;

        img {
            height: 100%;
        }
    }
}

    
</style>