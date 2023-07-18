<script >
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import LoaderComponent from './components/LoaderComponent.vue';
import axios from 'axios'
import {store} from './store'

export default {
    components: {
        HeaderComponent,
        MainComponent,
        LoaderComponent
    },
    data (){
        return {
            cards: [],
            isLoad: false,
            store
        }
    },
    methods: {
        
    },
    created() {
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=200&offset=0')
        .then(response => {
            console.log(response.data.data);
            this.store.cards = response.data.data;
        });

        setTimeout(() => {
        this.isLoad = true;
        }, 4000);
    },
    };
</script>

<template>

    
    <LoaderComponent v-if="isLoad == false"/>
    
    <div v-else>
        <HeaderComponent />
        <MainComponent />
    </div>
    

</template>

<style lang="scss">
@use "./assets/scss/main.scss";

</style>
