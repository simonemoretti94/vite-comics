<script>

import appcards from './appcards.vue';

export default {
    name: 'appheader',
    components: {
        appcards,
    },

    data() {
        return {
            /* appcards.vue array */
            cardsArray: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": 19.99,
                    "series": "Action Comics",
                    "type": "comic book",
                    "tag": 'comic',
                    "visibility": true,
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": 3.99,
                    "series": "American Vampire 1976",
                    "type": "comic book",
                    "tag": 'drama',
                    "visibility": true,
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": 14.99,
                    "series": "Aquaman",
                    "type": "graphic novel",
                    "tag": 'novel',
                    "visibility": true,
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": 7.99,
                    "series": "Batgirl",
                    "type": "comic book",
                    "tag": 'drama',
                    "visibility": true,
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": 3.99,
                    "series": "Batman",
                    "type": "comic book",
                    "tag": 'comic',
                    "visibility": true,
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": 9.99,
                    "series": "Batman Beyond",
                    "type": "comic book",
                    "tag": 'novel',
                    "visibility": true,
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": 13.99,
                    "series": "Batman/Superman",
                    "type": "comic book",
                    "tag": 'drama',
                    "visibility": true,
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": 16.99,
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                    "tag": 'novel',
                    "visibility": true,
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": 5.99,
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                    "tag": 'comic',
                    "visibility": true,
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": 11.99,
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                    "tag": 'drama',
                    "visibility": true,
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": 4.99,
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                    "tag": 'comic',
                    "visibility": true,
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": 16.99,
                    "series": "Catwoman",
                    "type": "graphic novel",
                    "tag": 'novel',
                    "visibility": true,
                }
            ],

            /* tagSelected and priceSelected's servants */
            tagVar: '',
            priceVar: '',
        }
    },
    methods: {
        /* appheader main tag select filter function */
        tagSelected(value, event) {

            //console.log('value: ', value, '$event: ', event);

            /* assigning value to external tagVar for future filterings */
            this.tagVar = value;

            this.cardsArray.forEach(element => {

                if (value === '') {
                    if (element.visibility === false) {
                        element.visibility = true;
                    }
                }
                else if (element.tag.includes(value)) {

                    element.visibility = !element.visibility;

                }
                else {
                    if (element.visibility === false) {
                        element.visibility = true;
                    }
                }
            });

        },

        /* appheader main select price filter function */
        priceSelected(value, event) {


            value = Number(value);

            /* assigning value to external priceVar for future filterings */
            this.priceVar = value;

            this.cardsArray.forEach(element => {

                if (value === 0) {
                    if (element.visibility === false) {
                        element.visibility = true;
                    }
                }
                else if (element.price < value && element.price >= (value - 4)) {
                    element.visibility = true;
                }
                else {
                    element.visibility = false;
                }
            });
        },

        bothSelectTags() {
            console.log('bothselect tags: ', this.tagVar, ' ', this.priceVar);
            this.cardsArray.forEach(element => {
                if (this.tagVar === '' || this.priceVar === 0) {
                    console.log('A value is missing: 1) tagvar ', this.tagVar, '2) pricevar ', this.priceVar);
                }
                else if ((element.price < this.priceVar && element.price >= (this.priceVar - 4)) && element.tag === this.tagVar) {
                    element.visibility = true;
                }
                else {
                    element.visibility = false;
                }
            });
        }
    }
}
</script>

<template>
    <header>
        <div class="container d-flex justify-content-between align-items-center">
            <img class="logo" src="../assets/img/header&sub/sub_1/dc-logo.png" alt="dc-logo">
            <ul>
                <li href="">characters</li>
                <li href="">comics</li>
                <li href="">movies</li>
                <li href="">tv</li>
                <li href="">games</li>
                <li href="">collectibles</li>
                <li href="">videos</li>
                <li href="">fans</li>
                <li href="">news</li>
                <li href="">shop</li>
            </ul>
        </div>
    </header>

    <main class="d-flex flex-column justify-content-evenly align-items-center">

        <div id="container_cards" class="container d-flex justify-content-center align-items-center flex-wrap">
            <appcards v-for="(card, index) in cardsArray" :visibility="card.visibility" :card="card" :index="index">
            </appcards>
        </div>

        <div id="div_wrapper" class="col-5 d-flex flex-row justify-content-center align-items-center my-3">

            <select name="filter" id="cards_filter" v-on:change="tagSelected($event.target.value, $event)">
                <option value="">All tags</option>
                <option value="comic">Comic</option>
                <option value="drama">Drama</option>
                <option value="novel">Novel</option>
            </select>


            <select name="filter" id="prices_filter" v-on:change="priceSelected($event.target.value, $event)">
                <option value="">All prices</option>
                <option value="5">1&euro; to 5&euro;</option>
                <option value="10">6&euro; to 10&euro;</option>
                <option value="15">11&euro; to 15&euro;</option>
                <option value="20">16&euro; to 20&euro;</option>
            </select>

            <button v-on:click="bothSelectTags()">{{ tagVar }} + {{ priceVar }}</button>
        </div>


    </main>

    <footer class="d-flex">

        <div class="container d-flex justify-content-between ">
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
    position: fixed;
    z-index: 1;
    width: 100%;
    min-height: 80px;
    font-family: 'Open Sans', sans-serif;
    display: flex;
    justify-content: center;

    background: linear-gradient(45deg, #000000, #cccccc, #ffffff);
    border-bottom: solid .25px #cccccc;

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

            & li {
                color: var(--main-dark);
                text-decoration: none;
                text-transform: uppercase;
                list-style: none;
                margin: auto .4rem;
                font-size: .6rem;
                font-weight: bolder;
            }

            & li:hover {
                font-weight: 800;
                color: var(--blue-comics);
                border-bottom: solid 2px var(--blue-comics);
            }
        }
    }
}

main {
    min-height: 80px;
    padding-top: 80px;
    background-color: black;
    color: var(--main-light);
    font-family: 'Open Sans', sans-serif;

    & .container {
        & p {
            margin-top: 1rem;
            font-weight: bolder;
        }
    }

    & select {
        margin: auto .2rem;
    }

    & #div_wrapper {
        position: relative;

        & #cards_filter {
            background-color: var(--blue-comics);
            padding: .2rem .45rem;
            border-radius: 10px;

            color: white;
            text-shadow: .5px .5px black;

            & option {
                background-color: rgb(71, 186, 214);
                color: white;
                text-align: center;
            }

        }

        & #prices_filter {
            background-color: var(--green-select);
            padding: .2rem .45rem;
            border-radius: 10px;

            & option {
                background-color: rgb(48, 211, 97);
                color: white;
                text-align: center;
            }
        }

        & button {
            position: absolute;
            top: 120%;
            left: 42%;
            padding: .2rem;
            border: solid 1px lightblue;
            background-color: var(--blue-comics);
            border-radius: 10px;
            text-transform: capitalize;
            font-size: small;
            font-weight: 500;
            color: white;
            text-shadow: -1px 1px black;


            cursor: pointer;
        }

        & button:hover {
            color: black;
            background-color: red;
            transform: scale(.8);
        }

    }
}

footer {
    min-height: 100px;
    background: linear-gradient(var(--blue-comics), #0063c6, var(--blue-comics));
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