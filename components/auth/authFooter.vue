<template>
  <div class="d-none d-lg-block">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="text-center py-4">
            <nuxt-link to=""><img src="~/static/img/playstore.png"></nuxt-link>
            <nuxt-link to=""><img src="~/static/img/appstore.png"></nuxt-link>
          </div>
        </div>
        <div class="col-12">
          <div class="d-flex align-items-center justify-content-around gap-2 mb-4">
            <nuxt-link to="" class="btn border-0">Ketentuan Layanan</nuxt-link>
            <nuxt-link to="" class="btn border-0">Kebijakan & Privasi</nuxt-link>
            <nuxt-link to="" class="btn border-0">Pusat Bantuan</nuxt-link>
            <nuxt-link to="" class="btn border-0">Tentang Kami</nuxt-link>
            <nuxt-link to="" class="btn border-0">Kontak</nuxt-link>
          </div>
        </div>
      </div>
    </div>
    <div class="bg-light">
      <div class="container">
        <div class="row">
          <div class="col-12">
            <div class="d-flex align-items-center justify-content-between py-3">
              <div>&copy; Copyright 2021 LBH HKTI. All right reserved.</div>
              <div class="d-flex align-items-center gap-2">
                <nuxt-link to="" class="btn border-0"><Icon icon="ant-design:instagram-filled" style="font-size: 24px;" class=""/></nuxt-link>
                <nuxt-link to="" class="btn border-0"><Icon icon="akar-icons:twitter-fill" style="font-size: 24px;" class=""/></nuxt-link>
                <nuxt-link to="" class="btn border-0"><Icon icon="brandico:facebook" style="font-size: 24px;" class=""/></nuxt-link>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Icon } from '@iconify/vue2'

export default {

  name: 'authFooter',

  components:{
    Icon
  },

  data () {
    return {

    }
  }
}
</script>

<style lang="scss" scoped>
a{
  color: #2A2B2A;

  &:hover{
    color: #6C757D;
    text-decoration: none;
  }
}
</style>