<template>
  <div id="myApp">
    <nav-bar class="bg-blur"></nav-bar>
    <nuxt/>
    <Footer />
  </div>
</template>

<script>
import NavBar from '~/components/NavBar'
import Footer from '~/components/Footer'
export default {
  data () {
    return {

    }
  },
  components: { NavBar, Footer }
}
</script>

<style>
.bg-blur{
  backdrop-filter: invert();  
  -webkit-backdrop-filter: invert();
  background-color: rgba(93, 92, 95, .1);
  
}

#myApp {
  /* background-image: url('/static/bg.jpg'); */
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
</style>

