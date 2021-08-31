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
                  <h5 class="mb-4">Kode Verifikasi</h5>
                </div>
                <div class="col-12 col-lg-8 offset-lg-2 text-center">
                  <div class="text-center mb-4">Kode verifikasi berhasil terkirim ke alamat email anda <b>budiman@rockermail.com</b></div>
                  <form>
                    <div class="input-wrapper text-center">
                      <PincodeInput v-model="code" placeholder="" length="6"/>
                    </div>
                    <div class="text-center mb-4">
                      <small>Tidak mendapatkan kode verifikasi? kirim ulang <b>00:59</b><br> 
                      <nuxt-link to="" class="text-danger">Kirim Ulang</nuxt-link></small>
                    </div>
                    <button type="button" class="btn btn-success btn-lg btn-block" @click="showAlert()">Konfirmasi</button>
                  </form>
                </div>
              </div>
            </div>
          </div>
          <Sidebar />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import PincodeInput from 'vue-pincode-input'
import swal from 'sweetalert2'
window.Swal = swal

export default {

  name: 'verifications',

  components:{
    PincodeInput,
  },

  data () {
    return {
      code: ''
    } 
  },

  methods: {
    showAlert() {
      // Use sweetalert2
      Swal.fire(
        'Berhasil!',
        'Anda berhasil mengubah email',
        'success'
      );
    },
  },
}
</script>

<style lang="css" scoped>
</style>