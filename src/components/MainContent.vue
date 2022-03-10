<template>

    <main id="album">
        <div class="container">

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

        </div>
    </main>

</template>

<script>
export default {
    name: 'mainContent',
    
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