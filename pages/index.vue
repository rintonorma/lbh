<template>
  <div>
    <div class="sidebar-overlay"></div>
    <MainHeader @sidebar="openSidebar" />
    <section class="bg-dashboard">
      <div class="container">
        <div class="row">
          <div class="col-12 col-lg-8" id="main">
            <div class="card" id="formReport" :class="{ 'open': report }">
              <div class="card-body">
                <div class="position-relative mb-4">
                  <a class="text-secondary position-absolute start-0 d-block d-lg-none" @click="report = !report"><Icon icon="eva:arrow-back-outline" style="font-size: 24px;"/></a>
                  <h5 class="m-0 w-100 text-center d-block d-lg-none">Berikan Laporan</h5>
                  <h5 class="mb-3 d-none d-lg-block">Berikan Laporan</h5>
                </div>
                <FormReport />
              </div>
            </div>
            <div class="main-content py-lg-4">
              <div class="card mb-4">
                <div class="card-body text-center">
                  Anda belum memberikan laporan dan mendapatkan jawaban. Silahkan berikan laporan anda pada kolom laporan.
                </div>
              </div>
              <Thread />
            </div>
            <a class="btn btn-light shadow rounded-pill position-fixed bottom-0 end-0 m-2 d-flex align-items-center gap-2 px-4 py-3 border-0 d-block d-lg-none" @click="report = true"><Icon icon="fluent:compose-16-filled" style="font-size: 24px;" class=""/><span>Berikan Laporan</span></a>
          </div>
          <Sidebar :open="open" @sidebar="openSidebar" />
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
      open: false,
      report: false,
    }
  },
  methods: {
    openSidebar() {
      this.open = ! this.open
    },
  }
}
</script>

<style lang="scss" scoped>

</style>