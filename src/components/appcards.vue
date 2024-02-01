<script>
export default {
    name: 'appcard',
    data() {
        return {}
    },
    props: {
        card: Object,
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
#div_injected {
    & img {
        aspect-ratio: 1 / 1;
        padding: .5rem;
    }

    & p {
        font-size: x-small;
    }
}
</style>