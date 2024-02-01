<script>

import appcards from './appcards.vue';

export default {
    name: 'appheader',
    components: {
        appcards,
    },

    data() {
        return {
            cardsArray: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                }
            ],
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

        <div class="container d-flex align-items-center flex-wrap">
            <appcards v-for="card in cardsArray" :card="card"></appcards>
        </div>

    </main>

    <footer class="d-flex">

        <div class="container d-flex justify-content-evenly ">
            <div class="wrapper">
                <img src="../assets/img/header&sub/sub_3/buy-comics-digital-comics.png" alt="buy-digital-comics">
                <a>digital comics</a>
            </div>
            <div class="wrapper">
                <img src="../assets/img/header&sub/sub_3/buy-comics-merchandise.png" alt="buy-digital-comics">
                <a>digital comics</a>
            </div>
            <div class="wrapper">
                <img src="../assets/img/header&sub/sub_3/buy-comics-subscriptions.png" alt="buy-digital-comics">
                <a>digital comics</a>
            </div>
            <div class="wrapper">
                <img src="../assets/img/header&sub/sub_3/buy-comics-shop-locator.png" alt="buy-digital-comics">
                <a>digital comics</a>
            </div>
            <div class="wrapper">
                <img src="../assets/img/header&sub/sub_3/buy-dc-power-visa.svg" alt="buy-digital-comics"
                    style="font-size: .5rem; color: blue;">
                <a>digital comics</a>
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
        & .logo {
            width: 70px;
            aspect-ratio: 1 / 1;
        }

        & .logo:hover {
            transform: rotate(-10deg);
        }

        & ul {
            margin-top: 1rem;
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

            & a:hover {
                font-weight: 800;
                color: black;
                border-bottom: 0;
            }

            & .a_blue {
                padding-top: 2px;
                color: var(--blue-comics);
                border-bottom: solid 2px var(--blue-comics);
            }

        }
    }
}

main {
    min-height: 80px;
    background-color: black;
    color: var(--main-light);
    font-family: 'Open Sans', sans-serif;

    & .container {
        & p {
            margin-top: 1rem;
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
                max-width: 37px;
                aspect-ratio: 1 / 1;
            }

            & a {
                margin-top: 0.1rem;
                margin-left: .5rem;
                text-transform: uppercase;
                text-decoration: none;
                color: var(--main-light);
                font-size: .7rem;
                font-weight: 500;
            }
        }
    }

}
</style>