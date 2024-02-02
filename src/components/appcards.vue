<script>
export default {
    name: 'appcards',
    data() {
        return {}
    },
    props: {
        card: Object,
        index: Number,
        visibility: Boolean,
        price: Number,
    },

}
</script>

<template>
    <div v-if="visibility" :id="'div_injected_' + index" class="col-2 d-flex flex-column justify-content-center my-2">
        <img :src="card.thumb" :alt="card.type">
        <p id="p_name">{{ card.series }}</p>
        <p id="p_price">{{ card.price }}&euro;</p>
    </div>
</template>

<style scoped>
div[id^="div_injected"] {



    & img {
        aspect-ratio: 1 / 1;
        padding: .5rem;
    }

    & p {
        font-size: small;
        font-weight: 500;
    }

    & p#p_name {
        margin-bottom: 0;
        text-align: center;
        text-transform: uppercase;
        color: white;
    }

    & p#p_price {
        text-align: center;
        font-size: x-small;
        color: rgb(196, 196, 80);
    }

}

div[id^="div_injected"]:hover {
    filter: saturate(200%) contrast(120%);
    cursor: pointer;

    & p#p_name {
        font-weight: 600;

    }

    & p#p_price {
        font-weight: 400;
    }

    & img {
        transform: scale(.9);
        border-radius: 10px;
        box-shadow: 1px 1px black;
        filter: drop-shadow(1px 1px 1px white);
    }
}
</style>