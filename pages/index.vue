<template>
  <main>
    <Hero/>
  </main>
</template>

<script>
export default {
  components: {
    Hero: () => import('../components/Hero.vue')
  }
}
</script>

<style>

</style>
