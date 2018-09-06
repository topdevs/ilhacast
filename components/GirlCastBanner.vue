<template>
  <div class="container">
    <div>

      <div class="text">
        <h1>
          <slot></slot>
        </h1>
      </div>

    </div>  
  </div>
</template>

<script>
export default {
  data () {
    return {

    }
  }
}
</script>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
}

.text {
  text-align: center;
  flex: 1;
}
</style>
