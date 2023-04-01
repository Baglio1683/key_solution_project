<script>

export default {

    name: "AppHeader"

}

</script>

<template>
    <header>
        <div class="container-fluid">
            <div class="row justify-content-between align-items-center">
                <div class="col-3">
                    <img src="../style/img/key_logo.png" alt="">
                </div>

                <h1 class="col-3 text-center">
                    UNLOCK YOUR ENERGY
                </h1>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    
    height: 15vh;

    img {
        max-width: 100%;
    }

    h1 {
        color: #ed5b27;
        font-weight: 700;
        font-size: medium;
        margin-bottom: 0;
    }
}
</style>