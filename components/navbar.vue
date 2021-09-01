<template>
  <div>
    <nuxt-link to="" class="btn btn-light btn-block my-3 btnReport">3 Laporan</nuxt-link>
    <ul>
      <li>
        <nuxt-link to="/inbox" class="d-flex align-items-center gap-2">
          <Icon icon="bx:bxs-inbox" style="font-size: 18px;" class=""/>
          <span>Kotak Masuk</span>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/sent" class="d-flex align-items-center gap-2 active">
          <Icon icon="bx:bxs-send" style="font-size: 18px;" class=""/>
          <span>Laporan Terkirim</span>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/draft" class="d-flex align-items-center gap-2">
          <Icon icon="bi:file-earmark-fill" style="font-size: 18px;" class=""/>
          <span>Draf</span>
        </nuxt-link>
      </li>
      <li class="d-block d-lg-none">
        <nuxt-link to="/settings" class="d-flex align-items-center gap-2">
          <Icon icon="ci:settings-filled" style="font-size: 18px;" class=""/>
          <span>Pengaturan</span>
        </nuxt-link>
      </li>
      <li class="d-block d-lg-none">
        <nuxt-link to="/" class="d-flex align-items-center gap-2">
          <Icon icon="uis:signout" style="font-size: 18px;" class=""/>
          <span>Keluar</span>
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
import { Icon } from '@iconify/vue2'

export default {

  name: 'navbar',

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

  li{
    a{
      display: block;
      width: 100%;
      padding: 10px 15px;
      color: #2A2B2A;
      border-radius: 10px;
      border: 1px solid transparent;
      margin-bottom: 10px;

      &:hover{
        background: white;
        text-decoration: none;
        color: #2A2B2A;
        border: 1px solid #D6DBD5;
      }
    }
    .active{
      background: #CCE5B2;
      color: #DF0714;
    }
  }
}

@media (max-width: 767px){
  .btnReport{
    margin-top: 0!important;
    border-radius: 0;
  }
  ul{
    li{
      a{
        border-radius: 0;
      }
    }
  }
}
</style>