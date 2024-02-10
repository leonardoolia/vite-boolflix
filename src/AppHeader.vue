<script>
import axios from 'axios';
import SearchProduct from './components/SearchProduct.vue';
import { store } from './assets/data/store';
import { api } from './assets/data/index';
export default {
    name: 'AppHeader',
    components: { SearchProduct },
    methods: {
        searchProduct(product) {
            axios.get(`${api.baseUri}/search/movie?api_key=${api.apiKey}&query=${product}`)
                .then((res) => {
                    store.movies = res.data.results
                })
                .catch((err) => {
                    console.error(err)
                })
        }
    }
}
</script>

<template>
    <header>
        <h1>BOOLFLIX</h1>
        <SearchProduct buttonText="Trova" placeholder="Scrivi qui" @form-submit="searchProduct" />
    </header>
</template>

<style></style>