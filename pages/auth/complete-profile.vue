<template>
  <div>
    <div class="bg-auth p-4">
      <div class="container-fluid">
        <div class="row">
          <div class="col-12 col-lg-4 offset-lg-4">
            <div class="card">
              <div class="card-body p-5">
                <div class="position-relative mb-4">
                  <!-- <nuxt-link to="" class="text-secondary position-absolute start-0"><Icon icon="eva:arrow-back-outline" style="font-size: 24px;"/></nuxt-link> -->
                  <h4 class="m-0 w-100 text-center">Lengkapi Data Diri</h4>
                </div>
                <form>
                  <label for="input-name" class="text-secondary">Nama Lengkap</label>
                  <div class="input-group mb-3">
                    <input type="text" class="form-control form-control-lg" id="input-name" aria-describedby="input-name" placeholder="Nama Lengkap">
                  </div>
                  <label for="input-phone" class="text-secondary">Nomor Ponsel</label>
                  <div class="input-group mb-3">
                    <input type="number" class="form-control form-control-lg" id="input-phone" aria-describedby="input-phone" placeholder="Contoh. 8211067890">
                  </div>
                  <label for="input-address" class="text-secondary">Alamat</label>
                  <div class="input-group mb-3">
                    <input type="text" class="form-control form-control-lg" id="input-address" aria-describedby="input-address" placeholder="Jl. Selamat sentosa no.1 RT/RW">
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
                  <nuxt-link to="" class="btn btn-success btn-lg btn-block">Selesai</nuxt-link>
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
import Select2 from 'v-select2-component'

export default {

  name: 'complete-profile',

  components:{
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
#input-kel{
  display: none;
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
</style>