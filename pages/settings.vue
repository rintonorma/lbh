<template>
  <div>
    <MainHeader />
    <section class="bg-dashboard">
      <div class="container">
        <div class="row">
          <div class="col-12 col-lg-8">
            <div class="card">
              <div class="card-body">
                <div class="d-flex align-items-center justify-content-between">
                  <h5 class="mb-0">Pengaturan</h5>
                </div>
                asdasdsa
              </div>
            </div>
          </div>
          <div class="col-12 col-lg-4">
            <ProfileBar />
            <nuxt-link to="" class="btn btn-light btn-block my-3">3 Laporan</nuxt-link>
            <Navbar />
            <MainFooter />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import ProfileBar from '~/components/profileBar'
import { Icon } from '@iconify/vue2'

export default {

  name: 'settings',

  components:{
    ProfileBar,
    Icon
  },

  data () {
    return {

    }
  }
}
</script>

<style lang="css" scoped>
</style>