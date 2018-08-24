<template>
  <div class="container-flex container-shadow">
    <div class="container-item">
      <p>O melhor, mais top e mais pica ! </p>
    </div>
    <div class="container-item">
      <logo />
    </div>

    <div class="container-item align-right">
      <div class="">
        <a href="https://github.com/topdevs/ilhacast">
          <i class="fa fa-github-alt"> Github</i>
        </a>
      </div>
    </div>
  </div>
</template>
<style>
  p {
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    /* font-style: italic; */
  }

  a {
    text-decoration: none;  
    color: black;
  }
  .container-shadow {
    /* x y smoth strength */
    box-shadow: 0px 1px 10px 0px; 
    /* background-color: rgba(255, 255, 255, .9); */
    -webkit-backdrop-filter: blur(100px);
  }

  .container-flex {
    display: flex;
    flex-wrap: wrap; 
    flex-direction: row;
    width: 100%;
    /* padding 0 top 10 right 10 bottom 0 left */
    padding: 0px 10px 10px 0px; 
    align-items: center;
    justify-content: center;
    box-sizing: border-box;

  }
  .container-item {
    /* display: flex; */
    flex: 1;
    text-align: center;
    /* background: red; */
  }
  .align-right {
    text-align: right;
  }

  .align-left {
    text-align: left;
  }

</style>


<script>
import logo from '~/components/IlhacastLogo'
export default {
  components: {
    logo
  },
  data () {
    return {

    }
  },// end data

  mounted () {

  } // end mounted
}
</script>
