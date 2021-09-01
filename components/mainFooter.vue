<template>
  <div class="row menuBar">
    <div class="col-12 col-lg-6">
      <ul>
        <li>
          <nuxt-link to="">Tentang Kami</nuxt-link>
        </li>
        <li>
          <nuxt-link to="">Ketentuan Layanan</nuxt-link>
        </li>
        <li>
          <nuxt-link to="">Kebijakan & Privasi</nuxt-link>
        </li>
      </ul>
    </div>
    <div class="col-12 col-lg-6">
      <ul>
        <li>
          <nuxt-link to="">Pusat Bantuan</nuxt-link>
        </li>
        <li>
          <nuxt-link to="">Kontak</nuxt-link>
        </li>
      </ul>
    </div>
    <div class="col-12">
      <div class="d-flex align-items-center gap-5">
        <nuxt-link to=""><Icon icon="ant-design:instagram-filled" style="font-size: 24px;" class=""/></nuxt-link>
        <nuxt-link to=""><Icon icon="akar-icons:twitter-fill" style="font-size: 24px;" class=""/></nuxt-link>
        <nuxt-link to=""><Icon icon="brandico:facebook" style="font-size: 24px;" class=""/></nuxt-link>
      </div>
    </div>
    <div class="col-12">
      <small>&copy; Copyright 2021 LBH HKTI. All rights reserved.</small>
    </div>
  </div>
</template>

<script>
import { Icon } from '@iconify/vue2'

export default {

  name: 'mainFooter',

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
ul{
  list-style: none;
  padding-left: 0;
}
a{
  display: block;
  //width: 100%;
  color: #2A2B2A;
  margin-bottom: 10px;
  padding: 10px 0;

  &:hover{
    text-decoration: none;
    color: #6C757D;
  }
}
.menuBar{
  font-size: 14px;
  margin: 0;
}
</style>