<template>
  <Header/>
  <main class="wrapper">
    <Catalog/>
  </main>
  <Footer/>
</template>

<script>
import Header from '@/components/Header'
import Catalog from '@/components/Catalog'
import Footer from '@/components/Footer'

export default {
  name: 'Wrapper',
  components: {
    Header,
    Catalog,
    Footer
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
</style>
