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
                  <h5 class="mb-4">Pengaturan</h5>
                </div>
                <ul class="nav nav-pills nav-justified btn-group mb-3" id="pills-tab" role="tablist">
                  <li class="nav-item btn p-0 overflow-hidden" role="presentation">
                    <a class="nav-link active" id="pills-home-tab" data-toggle="pill" href="#pills-home" role="tab" aria-controls="pills-home" aria-selected="true">Profil</a>
                  </li>
                  <li class="nav-item btn p-0 overflow-hidden" role="presentation">
                    <a class="nav-link" id="pills-profile-tab" data-toggle="pill" href="#pills-profile" role="tab" aria-controls="pills-profile" aria-selected="false">Akun</a>
                  </li>
                </ul>
                <div class="tab-content" id="pills-tabContent">
                  <div class="tab-pane fade show active" id="pills-home" role="tabpanel" aria-labelledby="pills-home-tab">
                    <form>
                      <label for="input-name" class="text-secondary">Nama Lengkap</label>
                      <div class="input-group mb-3">
                        <input type="text" class="form-control form-control-lg" id="input-name" aria-describedby="input-name" value="Budiman Mulianto">
                      </div>
                      <label for="input-phone" class="text-secondary">Nomor Ponsel</label>
                      <div class="input-group mb-3">
                        <input type="number" class="form-control form-control-lg" id="input-phone" aria-describedby="input-phone" value="08211067890">
                      </div>
                      <label for="input-address" class="text-secondary">Alamat</label>
                      <div class="input-group mb-3">
                        <input type="text" class="form-control form-control-lg" id="input-address" aria-describedby="input-address" value="Jl. Selamat sentosa no.1 RT/RW">
                      </div>
                      <div class="row">
                        <div class="col-12 col-lg-6">
                          <label for="input-kel" class="text-secondary">Kelurahan</label>
                          <div class="input-group mb-3">
                            <Select2 v-model="valueKel" :options="inputKel" :settings="{ width: '100%' }" @change="myChangeEvent($event)" @select="mySelectEvent($event)" placeholder="Pilih Kelurahan" id="input-kel" class="form-control form-control-lg p-0 py-2"/>
                          </div>
                        </div>
                        <div class="col-12 col-lg-6">
                          <label for="input-kec" class="text-secondary">Kecamatan</label>
                          <div class="input-group mb-3">
                            <Select2 v-model="valueKec" :options="inputKec" :settings="{ width: '100%' }" @change="myChangeEvent($event)" @select="mySelectEvent($event)" placeholder="Pilih Kecamatan" id="input-kec" class="form-control form-control-lg p-0 py-2"/>
                          </div>
                        </div>
                      </div>
                      <!-- <label for="input-city" class="text-secondary">Kota/Kabupaten</label>
                      <div class="input-group mb-3">
                        <input type="text" class="form-control form-control-lg" id="input-city" aria-describedby="input-city" placeholder="Kota/Kabupaten">
                      </div> -->
                      <label for="input-city" class="text-secondary">Kota/Kabupaten</label>
                      <div class="input-group mb-3">
                        <Select2 v-model="valueCity" :options="inputCity" :settings="{ width: '100%' }" @change="myChangeEvent($event)" @select="mySelectEvent($event)" placeholder="Pilih Kota/Kabupaten" id="input-city" class="form-control form-control-lg p-0 py-2"/>
                      </div>
                      <label for="input-ktp" class="text-secondary">Lampirkan KTP</label>
                      <div class="input-group mb-3">
                        <div class="custom-file">
                          <input type="file" class="custom-file-input" id="inputGroupFile02">
                          <label class="custom-file-label" for="inputGroupFile02" aria-describedby="inputGroupFileAddon02">Pilih berkas</label>
                        </div>
                      </div>
                      <div class="d-flex align-items-center justify-content-end gap-2">
                        <nuxt-link to="" class="btn btn-light text-dark btn-lg px-5">Batal</nuxt-link>
                        <nuxt-link to="" class="btn btn-success btn-lg px-5">Simpan</nuxt-link>
                      </div>
                    </form>
                  </div>
                  <div class="tab-pane fade" id="pills-profile" role="tabpanel" aria-labelledby="pills-profile-tab">
                    <ul>
                      <li><nuxt-link to="" class="btn btn-transparent border-0 text-start btn-lg btn-block">Ubah email</nuxt-link></li>
                      <li><nuxt-link to="" class="btn btn-transparent border-0 text-start btn-lg btn-block">Hapus akun</nuxt-link></li>
                      <li><nuxt-link to="" class="btn btn-transparent border-0 text-start text-danger btn-lg btn-block">Keluar</nuxt-link></li>
                    </ul>
                  </div>
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
import Sidebar from '~/components/sidebar'
import { Icon } from '@iconify/vue2'
import Select2 from 'v-select2-component'

export default {

  name: 'settings',

  components:{
    Sidebar,
    Icon,
    Select2
  },

  data () {
    return {
      valueKel: '',
      inputKel: ['kelurahan1', 'kelurahan2', 'kelurahan3'],
      valueKec: '',
      inputKec: ['kecamatan1', 'kecamatan2', 'kecamatan3'],
      valueCity: '',
      inputCity: ['kota1', 'kota2', 'kota3']
    }
  },

  methods: {
      myChangeEvent(val){
          console.log(val);
      },
      mySelectEvent({id, text}){
          console.log({id, text})
      }
  }
}
</script>

<style lang="scss">
.nav-pills .nav-link {
  border-radius: 0;
  background: #D6DBD5;
  color: #6C757D;
}
.nav-pills .nav-link.active, .nav-pills .show > .nav-link {
    color: #2a2b2a;
    background-color: transparent;
}
.select2-container--default{
 .select2-selection--single{
    background-color: transparent;
    border: 1px solid transparent;
    border-radius: 4px;
 }
}
.custom-file {
  height: calc(2.1em + 0.75rem + 2px);
  font-size: 1.25rem;

  .custom-file-input {
    height: calc(2.1em + .75rem + 2px); 
  }

  .custom-file-label {
    height: calc(2.1em + 0.75rem + 2px);
    line-height: 2.1;

    &:after {
      height: calc(2.1em + 0.75rem);
      line-height: 2.1;
      content: "Pilih";
      padding: 0.375rem 1.75rem;
    }
  }
}
ul{
  list-style: none;
  padding-left: 0;
}
</style>