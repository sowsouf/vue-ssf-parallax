<template>
  <div class="home">
    <h1>Welcome to homepage, do what you want</h1>
    <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
    <ssf-parallax image="https://www.visitportugal.com/sites/www.visitportugal.com/files/mediateca/23_660x371.jpg" power="3">
      <template slot="overlay-content">Heeeeeeey</template>
    </ssf-parallax>
    <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
  </div>
</template>

<script>

  import SsfParallax from "../../SsfParallax/components/Main";

  export default {

    name: 'Home',

    components: { SsfParallax },

    data() {
      return {}
    },

    created() {
    },

    methods: {}

  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
