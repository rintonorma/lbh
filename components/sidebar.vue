<template>
  <div class="col-12 col-lg-4">
    <ProfileBar />
    <Navbar />
    <MainFooter />
  </div>
</template>

<script>
import ProfileBar from '~/components/profileBar'
import Navbar from '~/components/navbar'
import MainFooter from '~/components/mainFooter'
export default {

  name: 'sidebar',

  components:{
    ProfileBar,
    Navbar,
    MainFooter
  },

  data () {
    return {

    }
  }
}
</script>

<style lang="css" scoped>
</style>