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
        <div class="container d-flex justify-content-between align-items-center">
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
    </header>

    <main class="d-flex justify-content-center">

        <div class="container d-flex justify-content-start align-items-center">
            <p>--&gt; Content goes here &lt;--</p>
        </div>

    </main>
</template>


<style scoped>
header {
    min-height: 80px;
    background-color: var(--main-light);
    font-family: 'Open Sans', sans-serif;
    display: flex;
    justify-content: center;

    & .container {

        width: 80%;

        & .logo {
            width: 70px;
            aspect-ratio: 1 / 1;
        }
    }
}

main {
    min-height: 80px;
    background-color: black;
    color: var(--main-light);
    font-family: 'Open Sans', sans-serif;

    & .container {
        width: 80%;

        & p {
            font-weight: bolder;
        }
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