<script>
import SearchBar from "./components/SearchBar.vue";
import axios from 'axios';

export default {
    data() {
        return {
            title: "BoolFlix",
            movieList: [],
        }
    },

    components: {
        SearchBar
    },

    methods: {
        fetchMovies(query) {
            axios.get(`https://api.themoviedb.org/3/search/movie?api_key=14ae40f822e70b609bb2418462eb935d&query=${query}`)
                .then((response) => {
                    this.movieList = response.data.results;
                })
        },
    },
};
</script>

<template>
    <SearchBar :title="title" @search="fetchMovies" />

    <ul>
        <li v-for="movie in movieList">{{ movie.original_title }}</li>
        <li v-for="movie in movieList">{{ movie.original_language }}</li>
        <li v-for="movie in movieList">{{ movie.vote_average }}</li>
    </ul>
</template>

<style lang="scss"></style>
