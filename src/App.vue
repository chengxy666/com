<template>
  <div id="app">
    <Header></Header>
    <router-view/>
    <Footer></Footer>
  </div>
</template>

<style>
</style>
<script>
import Header from './components/Header'
import Footer from './components/Footer'
export default {
  components:{
    Header,
    Footer
  }
}
</script>
