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

@import "../assets/scss/variabili.scss";

header {
    min-height: 76px;
    background-color: $colorsec;
    padding: 10px 20px;

    .logo {
        width: 46px;
        height: 46px;

        img {
            height: 100%;
        }
    }
}

    
</style>