<template>
  <div class="logo-container" >
    <!-- <div>
      <svg @mouseover="drawLogo" 
        width="170"
        height="51"
        xmlns="http://www.w3.org/2000/svg">
          <text 
            
          
            font-family="Helvetica, Arial, sans-serif"
            font-size="48"
            y="50"
            x="80"
            text-anchor="middle" 
            stroke-width="1.9" 
            fill="none">{{ this.name }}
          </text>
      </svg>
    </div> -->

    <div>
      <svg  @mouseover="drawLogo"
        width="170"
        height="51"
        xmlns="http://www.w3.org/2000/svg"
        >
          <text 
            class="logo"
            stroke="#f57600" 
            font-family="Helvetica, Arial, sans-serif"
            font-size="48"
            y="50"
            x="80"
            text-anchor="middle" 
            stroke-width="1.2" 
            stroke-dashoffset="160"
            stroke-dasharray="160"
            fill="none">{{ this.name }}
          </text>
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  props: ['name'],
  data() {
    return {
      logo: null
    }
  }, // end data

  methods: {
    drawLogo () {
          const tl = new TimelineMax()
          
        TweenMax.fromTo(this.logo, 4,{
          strokeDashoffset: 180,
          strokeDasharray: 180,
        },
        {
          strokeDashoffset: 0,
          strokeDasharray: 160,
          // ease: Bounce.easeOut,
          // repeat: -1
          // yoyo: true
        })
    }
  }, // end methods

  mounted () {
    this.logo = document.querySelector('.logo')
    setTimeout(this.drawLogo, 1000);
  } // end mounted
}
</script>

<style>
.logo-container {
  display: flex;
  justify-content: center;
}

/* .logo-container div:first-child {
  position: relative;
  float: left;
}

.logo-container div:last-child {
  position: absolute;
} */
</style>

