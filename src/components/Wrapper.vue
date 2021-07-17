<template>
<main class="wrapper">
  <Header/>
  <Catalog/>
</main>
</template>

<script>
import Catalog from '@/components/Catalog'
import Header from '@/components/Header'

export default {
  name: 'Wrapper',
  components: {
    Catalog,
    Header
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
</style>
