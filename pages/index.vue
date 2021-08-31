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
          <Sidebar />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import MainHeader from '~/components/mainHeader'
import FormReport from '~/components/formReport'
import Thread from '~/components/thread'
import Sidebar from '~/components/sidebar'
import { Icon } from '@iconify/vue2'

export default {

  name: 'index',

  components:{
    MainHeader,
    FormReport,
    Thread,
    Sidebar,
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