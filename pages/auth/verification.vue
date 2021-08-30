<template>
  <div>
    <div class="bg-auth p-4">
      <div class="container-fluid">
        <div class="row">
          <div class="col-12 col-lg-4 offset-lg-4">
            <div class="card">
              <div class="card-body p-5">
                <div class="position-relative mb-4">
                  <nuxt-link to="" class="text-secondary position-absolute start-0"><Icon icon="eva:arrow-back-outline" style="font-size: 24px;"/></nuxt-link>
                  <h4 class="m-0 w-100 text-center">Kode Verifikasi</h4>
                </div>
                <div class="text-center mb-4">Kode verifikasi berhasil terkirim ke alamat email anda <b>budiman@rockermail.com</b></div>
                <form>
                  <div class="input-wrapper">
                    <PincodeInput v-model="code" placeholder="" length="6"/>
                  </div>
                  <div class="text-center mb-4">
                    <small>Tidak mendapatkan kode verifikasi?<br>
                    kirim ulang <b>00:59</b><br> 
                    <nuxt-link to="" class="text-danger">Kirim Ulang</nuxt-link></small>
                  </div>
                  <nuxt-link to="" class="btn btn-success btn-lg btn-block">Konfirmasi</nuxt-link>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <AuthFooter />
  </div>
</template>

<script>
import { Icon } from '@iconify/vue2'
import PincodeInput from 'vue-pincode-input'

export default {

  name: 'verification',

  components:{
    Icon,
    PincodeInput
  },

  data () {
    return {
      code: '',
    }
  }
}
</script>

<style lang="scss" scoped>

</style>