<script >
import {store} from '../store.js';

export default {
    name: "MainComponent",
data (){
    return {
        store
    }
},
methods: {

},
};
</script>

<template>
    <main>

        <div class="container">

            <select class="form-select" aria-label="Default select example">
                <option selected 
                        disabled
                        >Select Archetype</option>
                <option v-for="(archeType, indexA) in store.archetype" :key="indexA" value="archeType.archetype_name">{{archeType.archetype_name}}</option>
            </select>

            <div class="founded">
                Found {{store.cards.length}} Cards
            </div>
            <div class="my-row">
                <div class="col-12 col-sm-6 col-md-4 col-lg-3"
                        v-for="(singleCard, i) in store.cards" :key="i">
                    <div class="card-container">
                        <div class="img-container img-fluid">
                            <img :src="singleCard.card_images[0].image_url" alt="singleCard.name">
                        </div>
                        <div class="info-card">
                            <h2>
                                {{singleCard.name}}
                            </h2>
                            <h3>
                                {{singleCard.archetype}}
                            </h3>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>

main {
    background-color: chocolate;
    padding: 50px 0px;

    select {
        width: 300px;
        margin-bottom: 30px;
    }
    .founded {
            background-color: rgb(30, 30, 30);
            color: white;
            padding: 20px;
        }
    .my-row {
        display: flex;
        flex-wrap: wrap;
        padding: 30px;
        background-color: white;
    }

    .card-container {
        margin: 20px 0;
    
        .img-container {
            width: 100%;
            padding: 0 10px;

            img {
                width: 100%;
                display: block;
            }
        }

        .info-card{
            background-color: chocolate;
            text-align: center;
            padding-top: 10px;
            margin: 0 10px;
            line-height: 20px;
            height: 200px;

            h2 {
                color: white;
            }
        }
    }
}

</style>