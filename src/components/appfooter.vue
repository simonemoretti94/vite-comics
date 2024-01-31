
<script>
export default {
    name: 'appfooter',
    data() {
        return {

        }
    },
}
</script>

<template>
    <main class="d-flex justify-content-between align-items-center">

        <div class=" container d-flex justify-content-between align-items-center">
            <div id="start">
                <a>sign-up-now!</a>
            </div>

            <div id="end">
                <a>follow us</a>
                <div>
                    <img src="../assets/img/footer&sub/footer-facebook.png" alt="facebook_thumbnail">
                    <img src="../assets/img/footer&sub/footer-twitter.png" alt="twitter_thumbnail">
                    <img src="../assets/img/footer&sub/footer-youtube.png" alt="youtube_thumbnail">
                    <img src="../assets/img/footer&sub/footer-pinterest.png" alt="pinterest_thumbnail">
                    <img src="../assets/img/footer&sub/footer-periscope.png" alt="periscope_thumbnail">
                </div>
            </div>
        </div>

    </main>
</template>


<style scoped>
main {
    min-height: 60px;
    background-color: var(--main-dark);

    & .container {

        & div#start {

            & a {
                padding: .4rem .4rem;
                border: solid 1.7px var(--blue-comics);
                color: white;
                text-transform: uppercase;
                text-decoration: none;
                font-size: 55%;
                font-weight: bold;
            }

        }



        & div#end {
            display: flex;
            justify-content: space-between;

            & a {
                color: var(--blue-comics);
                text-transform: uppercase;
                text-decoration: none;
                font-weight: bolder;
                padding-top: .17rem;
                margin-right: .5rem;
            }

            & img {
                width: 20px;
                aspect-ratio: 1 / 1;
                margin: auto .3rem;
            }
        }
    }
}
</style>