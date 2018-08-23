<template>
  <div @mouseover="drawLogo">

    <svg width="170" height="51" xmlns="http://www.w3.org/2000/svg">
      <text 
      stroke="#f57600" 
      class="logo"
      font-family="Helvetica, Arial, sans-serif"
      font-size="48"
      y="50"
      x="80"
      text-anchor="middle" 
      stroke-width="1.2" 
      fill="none">ilhacast</text>
    
    </svg>

  </div>
</template>

<script>
export default {
  
  data() {
    return {
      logo: null
    }
  }, // end data

  methods: {
    drawLogo () {
          TweenMax.fromTo(this.logo, 3, {
          strokeDashoffset: 180,
          strokeDasharray: 180
        },
        {
          strokeDashoffset: 0
        })
    }
  }, // end methods

  mounted () {
    this.logo = document.querySelector('.logo')
  } // end mounted
}
</script>
