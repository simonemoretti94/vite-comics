
<script>
export default {
    name: 'appmain',
    data() {
        return {

        }
    },
}
</script>

<template>
    <main>
        <div class="container">

        </div>
    </main>

    <footer>

    </footer>
</template>


<style scoped>
main {

    min-height: 300px;
    background-image: url('../assets/img/main&sub/jumbotron.jpg');
    background-size: contain;
    filter: grayscale(100%);

    font-family: 'Open Sans', sans-serif;
    display: flex;
    justify-content: start;

}

footer {
    min-height: 80px;
    background-color: var(--main-dark);
    font-family: 'Open Sans', sans-serif;
    display: flex;
    justify-content: center;

}
</style>