<template>
  <div>
    <MainHeader @sidebar="openSidebar"/>
    <section class="bg-dashboard">
      <div class="container">
        <div class="row">
          <div class="col-12 col-lg-8" id="main">
            <div class="card">
              <div class="card-body">
                <div class="d-flex align-items-center justify-content-between">
                  <h5 class="mb-4">Ubah Email</h5>
                </div>
                <form>
                  <label for="input-email" class="text-secondary">Email</label>
                  <div class="input-group mb-3">
                    <input type="email" class="form-control form-control-lg" id="input-email" aria-describedby="input-email" value="budiman@rockermail.com">
                  </div>
                  <div class="d-flex align-items-center justify-content-end gap-2">
                    <nuxt-link to="/settings" class="btn btn-light text-dark btn-lg px-lg-5">Batalkan</nuxt-link>
                    <nuxt-link to="/verifications" class="btn btn-success btn-lg px-lg-5">Selanjutnya</nuxt-link>
                  </div>
                </form>
              </div>
            </div>
          </div>
          <Sidebar :open="open" @sidebar="openSidebar"/>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {

  name: 'changeEmail',

  data () {
    return {
      open: false
    }
  },

  methods:{
    openSidebar() {
      this.open = ! this.open 
    }
  }
}
</script>

<style lang="css" scoped>
</style>