<script>
import appheader from './components/appheader.vue';
import appmain from './components/appmain.vue';
import appfooter from './components/appfooter.vue';



export default {
  name: 'app',
  components: {
    appheader,
    appmain,
    appfooter,
  },
  data() {
    return {
      sentence: '',
      words: [],
    }
  },
  mounted() {
    for (let index = 0; index < 5; index++) {
      axios
        .get('https://flynn.boolean.careers/exercises/api/random/sentence')
        .then((response) => {
          /* always check what response contains */
          //console.log(response);

          /* pushing response.data.response to words array  */
          this.words.push(response.data.response);
          console.log('words array: ', this.words);
        });

    }
  },
}
</script>


<template>
  <appheader></appheader>
  <!-- 
  <div v-for="(element, index) in words">
    <h1 class="text-center text-white my-1">{{ element }}</h1>
  </div> -->

  <appmain></appmain>

  <appfooter></appfooter>
</template>

<style scoped></style>