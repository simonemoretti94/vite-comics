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

    <footer class="d-flex">

        <div class="container d-flex justify-content-evenly ">
            <div class="wrapper">
                <img src="../assets/img/header&sub/sub_3/buy-comics-digital-comics.png" alt="buy-digital-comics">
                <p>digital comics</p>
            </div>
            <div class="wrapper">
                <img src="../assets/img/header&sub/sub_3/buy-comics-merchandise.png" alt="buy-digital-comics">
                <p>digital comics</p>
            </div>
            <div class="wrapper">
                <img src="../assets/img/header&sub/sub_3/buy-comics-subscriptions.png" alt="buy-digital-comics">
                <p>digital comics</p>
            </div>
            <div class="wrapper">
                <img src="../assets/img/header&sub/sub_3/buy-comics-shop-locator.png" alt="buy-digital-comics">
                <p>digital comics</p>
            </div>
            <div class="wrapper">
                <img src="../assets/img/header&sub/sub_3/buy-dc-power-visa.png" alt="buy-digital-comics">
                <p>digital comics</p>
            </div>
        </div>

    </footer>
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

footer {
    min-height: 100px;
    background-color: var(--blue-comics);
    font-family: 'Open Sans', sans-serif;


    & .container {
        width: 80%;

        & .wrapper {
            width: calc((100% / 5) - 15px);
            display: flex;
            justify-content: center;
            align-items: center;

            & img {
                max-width: 40px;
                aspect-ratio: 1 / 1;
            }

            & p {
                margin-top: 1.1rem;
                margin-left: .4rem;
                text-transform: uppercase;
                color: var(--main-light);
                font-size: .7rem;
                font-weight: 500;
            }
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