
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

            <div id="wrapper" class="d-flex flex-row justify-content-start align-items-start ">
                <div class="d-flex flex-column justify-content-between ">
                    <ul>
                        <h5>dc comics</h5>
                        <a href="">characters</a>
                        <a href="">comics</a>
                        <a href="">movies</a>
                        <a href="">TV</a>
                        <a href="">games</a>
                        <a href="">videos</a>
                        <a href="">news</a>
                    </ul>
                    <ul>
                        <h5>shop</h5>
                        <a href="">shop DC</a>
                        <a href="">shop DC collectibles</a>
                    </ul>
                </div>
                <div class="d-flex flex-column justify-content-between ">
                    <ul>
                        <h5>dc</h5>
                        <a href="">terms of use</a>
                        <a href="">privacy policy (new)</a>
                        <a href="">add choices</a>
                        <a href="">advertising</a>
                        <a href="">jobs</a>
                        <a href="">subscriptions</a>
                        <a href="">talent workshops</a>
                        <a href="">CPSC certificates</a>
                        <a href="">ratings</a>
                        <a href="">shop help</a>
                        <a href="">contact us</a>
                    </ul>
                </div>
                <div class="d-flex flex-column justify-content-between ">
                    <ul>
                        <h5>sites</h5>
                        <a href="">DC</a>
                        <a href="">MAD magazine</a>
                        <a href="">DC kids</a>
                        <a href="">DC universe</a>
                        <a href="">DC power visa</a>
                    </ul>
                </div>
            </div>

        </div>
    </main>
</template>


<style scoped>
main {

    min-height: 250px;
    background-image: url('../assets/img/main&sub/jumbotron.jpg');
    background-size: contain;
    /* opacity: 0.5; */
    filter: grayscale(100%) brightness(100%) saturate(100%);



    font-family: 'Open Sans', sans-serif;
    display: flex;
    justify-content: start;

    & .container {
        width: 80%;

        & div#wrapper {
            margin-top: 1rem;

            & div {

                & ul {
                    display: flex;
                    flex-direction: column;
                    justify-content: start;

                    & h5 {
                        text-transform: uppercase;
                        font-size: 80%;
                        font-weight: bolder;
                        color: white;
                        text-align: left;
                        margin-bottom: .4rem;

                    }

                    & a {
                        text-transform: capitalize;
                        text-decoration: none;
                        word-spacing: .5px;
                        letter-spacing: .2px;
                        font-weight: 500;
                        font-size: 70%;
                        color: var(--appmain-anchortags);
                        text-align: left;

                        margin-bottom: .1rem;
                    }
                }
            }


        }

    }

}

footer {
    min-height: 80px;
    background-color: var(--main-dark);
    font-family: 'Open Sans', sans-serif;
    display: flex;
    justify-content: center;

}
</style>