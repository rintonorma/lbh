<template>
  <div class="col-12 col-lg-4" id="sidebar" ref="sidebar" :class="{ 'open': open }">
    <a class="position-absolute top-0 end-0 z-index-1 bg-white rounded-pill shadow m-3 d-block d-lg-none" @click="closeSidebar()"><Icon icon="bx:bx-x" style="font-size: 32px;" class="text-dark"/></a>
    <ProfileBar />
    <Navbar />
    <MainFooter />
  </div>
</template>

<script>
import ProfileBar from '~/components/profileBar'
import Navbar from '~/components/navbar'
import MainFooter from '~/components/mainFooter'
import { Icon } from '@iconify/vue2'

export default {

  name: 'sidebar',
  props: {
    open: Boolean
  },
  components:{
    ProfileBar,
    Navbar,
    MainFooter,
    Icon
  },

  data () {
    return {

    }
  },

  methods: {
    closeSidebar() {
      // console.log('clicked')
      this.$emit('sidebar')
    }
  }
}
</script>

<style lang="css" scoped>
</style>