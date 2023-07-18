<script >
export default {
    name: "LoaderComponent",
    data (){
        return {

        }
    },
    methods: {

    }
};
</script>

<template>
    <div class="loading">
        ...Loading...
    </div>
    <div class="spinner">
        <!-- <i class="fa-solid fa-dharmachakra fa-5x"></i> -->
        <img src="https://i.pinimg.com/564x/b3/60/94/b3609486bb72a022f452cd23fa90975b.jpg" alt="">
    </div>
    

</template>

<style lang="scss" scoped>

.spinner {
    text-align: center;
    font-size: 5em;
    animation-name: giro-infinito;
    animation-duration: 3s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
    width: 300px;
    margin: 100px auto;

    img {
        width: 100%;
    }

    @keyframes giro-infinito {
        0% {
            transform: rotate(0deg);
        }
        100% {
            transform: rotate(360deg);
        }
        
    }
}

.loading {
    font-size: 30px;
}


</style>
