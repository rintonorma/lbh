<template>
  <div>
    <div class="bg-auth p-4">
      <div class="container-fluid">
        <div class="row">
          <div class="col-12 col-lg-4 offset-lg-4">
            <div class="card">
              <div class="card-body p-5">
                <div class="text-center mb-4">
                  <img src="~/static/img/logo.png">
                </div>
                <h5 class="text-center mb-4">Belum punya akun? <nuxt-link to="" class="text-danger">Buat akun</nuxt-link></h5>
                <form>
                  <label for="input-email" class="text-secondary">Email</label>
                  <div class="input-group mb-3">
                    <input type="email" class="form-control form-control-lg" id="input-email" aria-describedby="input-email" placeholder="nama@email.com">
                  </div>
                  <nuxt-link to="" class="btn btn-success btn-lg btn-block">Masuk</nuxt-link>
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

  name: 'signin',

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