<script>

export default {
    props: {
        title: String,
    },
};
</script>

<template>
    <nav class="navbar bg-light">
        <div class="container-fluid">
            <a class="navbar-brand">{{ title }}</a>
            <form class="d-flex" role="search">
                <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                <button class="btn btn-outline-success" type="submit">Search Movies and Series</button>
            </form>
        </div>
    </nav>
</template>

<style lang="scss" scoped></style>