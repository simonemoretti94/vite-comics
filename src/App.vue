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
  }
}
</script>


<template>
  <appheader></appheader>

  <appmain></appmain>

  <appfooter></appfooter>
</template>

<style scoped></style>