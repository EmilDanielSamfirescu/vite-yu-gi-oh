<script >
export default {
    name: "HeaderComponent",
data (){
    return {

    }
},
methods: {

}
};
</script>

<template>
    <header class="d-flex">

        <div class="img-container align-middle">
            <img src="../assets/img/pngegg.png" alt="">
        </div>

        <h1>
            Yu-Gi-Oh Api
        </h1>

    </header>
</template>

<style lang="scss" scoped>

header {
    padding-left: 30px;
    height: 100px;

    h1 {
        line-height: 100px;
        padding-left: 30px;
    }
    .img-container {
        width: 100px;
        display: block;
    
        img {
            width: 100%;
            display: block;
        }
    }

}

</style>