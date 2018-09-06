<template>
  <div class="index">
    <section class="section">
      <girl-cast-banner>Aqui você encontra loucos convictos
      </girl-cast-banner>
    </section>
     <section class="section">
      <h1>teste</h1>
    </section>
  </div>
</template>

<script>
import GirlCastBanner from '~/components/GirlCastBanner'

export default {
  components: {
    GirlCastBanner
  }
}
</script>

<style scoped>
.index {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;

}

.section {
  flex: 1;
}

</style>

