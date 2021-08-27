<template>
  <div>
    <MainHeader />
    <section class="bg-dashboard">
      <div class="container">
        <div class="row">
          <div class="col-12 col-lg-8">
            <div class="card">
              <div class="card-body">
                <h5 class="mb-3">Berikan Laporan</h5>
                <FormReport />
              </div>
            </div>
            <div class="main-content py-4">
              <div class="card mb-4">
                <div class="card-body text-center">
                  Anda belum memberikan laporan dan mendapatkan jawaban. Silahkan berikan laporan anda pada kolom laporan.
                </div>
              </div>
              <Thread />
            </div>
          </div>
          <div class="col-12 col-lg-4">
            <div class="d-flex align-items-center gap-2">
              <div class="avatar avatar-xl">
                <img src="~/static/img/photo-1519993796861-26556330a4a9.jpeg">
              </div>
              <div class="d-grid gap-2">
                <div class="d-flex align-items-center gap-2">
                  <h5 class="m-0">Budiman Mulianto</h5>
                  <Icon icon="bi:check-circle-fill" style="font-size: 18px;" class="text-primary"/>
                </div>
                <div class="d-flex align-items-center gap-2">
                  <Icon icon="ci:location" style="font-size: 18px;" class="text-danger"/>
                  Kab. Majalengka
                </div>
              </div>
            </div>
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
import MainHeader from '~/components/mainHeader'
import FormReport from '~/components/formReport'
import Thread from '~/components/thread'
import Navbar from '~/components/navbar'
import MainFooter from '~/components/mainFooter'
import { Icon } from '@iconify/vue2'

export default {

  name: 'index',

  components:{
    MainHeader,
    MainFooter,
    FormReport,
    Thread,
    Navbar,
    Icon
  },

  data () {
    return {

    }
  }
}
</script>

<style lang="scss" scoped>

</style>