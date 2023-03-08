<script>

export default {

    data() {
        return {
            term: ''
        }
    },

    props: {
        title: String,
    },

    emits: ['search'],
};
</script>

<template>
    <nav class="navbar bg-light">
        <div class="container-fluid">
            <a class="navbar-brand">{{ title }}</a>
            <form class="d-flex" role="search" @submit.prevent="$emit('search', term)">
                <input v-model="term" class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                <button class="btn btn-outline-success" type="submit">Search Movies and
                    Series</button>
            </form>
        </div>
    </nav>
</template>

<style lang="scss" scoped></style>