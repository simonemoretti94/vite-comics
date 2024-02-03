
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
    <div id="background"></div>
    <main>
        <div class="container">

            <div id="wrapper" class="d-flex flex-row justify-content-start align-items-start ">
                <div class="d-flex flex-column justify-content-between align-items-start">
                    <ul class="list-unstyled">
                        <h5>dc comics</h5>
                        <li href="">characters</li>
                        <li href="">comics</li>
                        <li href="">movies</li>
                        <li href="">TV</li>
                        <li href="">games</li>
                        <li href="">videos</li>
                        <li href="">news</li>
                    </ul>
                    <ul class="list-unstyled">
                        <h5>shop</h5>
                        <li href="">shop DC</li>
                        <li href="">shop DC collectibles</li>
                    </ul>
                </div>
                <div class="d-flex flex-column justify-content-between align-items-start ">
                    <ul class="list-unstyled">
                        <h5>dc</h5>
                        <li href="">terms of use</li>
                        <li href="">privacy policy (new)</li>
                        <li href="">add choices</li>
                        <li href="">advertising</li>
                        <li href="">jobs</li>
                        <li href="">subscriptions</li>
                        <li href="">talent workshops</li>
                        <li href="">CPSC certificates</li>
                        <li href="">ratings</li>
                        <li href="">shop help</li>
                        <li href="">contact us</li>
                    </ul>
                </div>
                <div class="d-flex flex-column justify-content-between align-items-start">
                    <ul class="list-unstyled">
                        <h5>sites</h5>
                        <li href="">DC</li>
                        <li href="">MAD magazine</li>
                        <li href="">DC kids</li>
                        <li href="">DC universe</li>
                        <li href="">DC power visa</li>
                    </ul>
                </div>
            </div>

        </div>
    </main>
</template>


<style scoped>
main {
    background-image: url(../assets/img/main&sub/dc-logo-bg.png), url(../assets/img/footer&sub/footer-bg.jpg);
    background-repeat: no-repeat, repeat;
    background-position: right 150px top -40px, center;
    background-size: 350px, cover;
    position: relative;
    min-height: 250px;

    font-family: 'Open Sans', sans-serif;
    display: flex;
    justify-content: start;


    & .container {
        position: relative;
        top: 0;
        left: 0;

        & div#wrapper {
            margin-top: .45rem;

            & div {
                margin-right: 1rem;

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

                    & li {
                        text-transform: capitalize;
                        text-decoration: none;
                        word-spacing: .5px;
                        letter-spacing: .2px;
                        font-weight: 500;
                        font-size: 70%;
                        text-align: left;
                        color: var(--appmain-anchortags);
                        filter: drop-shadow(.1px .1px .1px white);

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