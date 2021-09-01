<template>
  <div>
    <div class="bg-auth p-lg-4">
      <div class="container-fluid">
        <div class="row">
          <div class="col-12 col-lg-4 offset-lg-4" id="main">
            <div class="card">
              <div class="card-body p-lg-5">
                <div class="text-center mb-4">
                  <img src="~/static/img/logo.png">
                </div>
                <h4 class="text-center mb-4">Lembaga Bantuan Hukum Himpunan Kerukunan Tani Indonesia</h4>
                <h5 class="text-center mb-4">Sudah punya akun? <nuxt-link to="/auth/signin" class="text-danger">Masuk</nuxt-link></h5>
                <form>
                  <label for="input-email" class="text-secondary">Email</label>
                  <div class="input-group mb-3">
                    <input type="email" class="form-control form-control-lg" id="input-email" aria-describedby="input-email" placeholder="nama@email.com">
                  </div>
                  <div class="text-center mb-4"><small>Dengan mendaftar, saya menyatakan bahwa saya setuju dengan <nuxt-link to="" class="text-danger">Ketentuan Layanan</nuxt-link> dan <nuxt-link to="" class="text-danger">Kebijakan Privasi</nuxt-link></small></div>
                  <nuxt-link to="/auth/verification" class="btn btn-success btn-lg btn-block">Selanjutnya</nuxt-link>
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
import AuthFooter from '~/components/auth/authFooter'
export default {

  name: 'signup',

  components:{
    AuthFooter,
  },

  data () {
    return {

    }
  }
}
</script>

<style lang="css" scoped>
</style>