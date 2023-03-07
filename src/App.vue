<script>
import SearchBar from "./components/SearchBar.vue";

export default {
    data() {
        return {
            title: "BoolFlix"
        }
    },

    components: {
        SearchBar
    },
};
</script>

<template>
    <SearchBar :title="title" />
</template>

<style lang="scss"></style>
