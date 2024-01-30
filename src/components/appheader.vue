<script>
export default {
    name: 'appheader',
    data() {
        return {

        }
    },
}
</script>

<template>
    <header>
        <div class="container">
            <div class="row">
                <img class="logo" src="../assets/img/header&sub/sub_1/dc-logo.png" alt="dc-logo">
                <ul>
                    <a href="">characters</a>
                    <a href="" class="a_blue">comics</a>
                    <a href="">movies</a>
                    <a href="">tv</a>
                    <a href="">games</a>
                    <a href="">collectibles</a>
                    <a href="">videos</a>
                    <a href="">fans</a>
                    <a href="">news</a>
                    <a href="">shop</a>
                </ul>
            </div>
        </div>
    </header>

    <main>

    </main>
</template>


<style scoped>
header {
    min-height: 80px;
    background-color: var(--main-light);
    font-family: 'Open Sans', sans-serif;
}

main {
    min-height: 120px;
    background-color: black;
    font-family: 'Open Sans', sans-serif;
}

.container {
    width: 70%;
    height: 80%;
    max-width: 1176px;
    margin: auto;
}

.row {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;



}

header .row {

    padding-top: .3rem;

    & .logo {
        width: 70px;
        aspect-ratio: 1 / 1;
    }
}

ul {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;

    & a {
        color: var(--main-dark);
        text-decoration: none;
        text-transform: uppercase;
        margin: auto .4rem;
        font-size: .6rem;
        font-weight: bolder;
    }

    & .a_blue {
        color: var(--blue-comics);
    }

}
</style>