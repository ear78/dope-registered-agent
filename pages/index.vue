<template>
  <b-container fluid>
      <Hero/>
      <Informative/>
  </b-container>
</template>

<script>
export default {
  components: {
    Hero: () => import('../components/Hero.vue'),
    Informative: () => import('../components/Informative.vue')
  }
}
</script>

<style>

</style>
