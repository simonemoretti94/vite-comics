<script>
export default {
    name: 'appcards',
    data() {
        return {}
    },
    props: {
        card: Object,
        index: Number,
    },

}
</script>

<template>
    <div id="div_injected" class="col-2 d-flex flex-column justify-content-center my-2">
        <img :src="card.thumb" :alt="card.type">
        <p class="text-center text-white text-uppercase">{{ card.series }}</p>
    </div>
</template>

<style scoped>

div[id^="div_injected"]{

    

    & img {
        aspect-ratio: 1 / 1;
        padding: .5rem;
    }

    & p {
        font-size: small;
        font-weight: 500;
    }
 
}

div[id^="div_injected"]:hover {
    filter:  saturate(200%) contrast(120%);
    cursor: pointer;

        & p {
            font-weight: 600;

        }

        & img {
            transform: scale(.9);
            border-radius: 10px;
            box-shadow: 1px 1px black;
            filter: drop-shadow(1px 1px 1px white);
        }
}

</style>