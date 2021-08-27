<template>
  <div class="bg-white shadow sticky-top">
    <div class="container">

      <nav class="navbar navbar-expand-lg navbar-light bg-transparent">
        <a class="navbar-brand" href="#"><img src="~/static/img/logo.png" width="67px"></a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav ml-auto">
            <li class="nav-item">
              <a class="nav-link" href="#"><Icon icon="clarity:notification-solid" style="font-size: 24px;" /></a>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                <Icon icon="ci:settings-filled" style="font-size: 24px;"/>
              </a>
              <div class="dropdown-menu dropdown-menu-right" aria-labelledby="navbarDropdown">
                <a class="dropdown-item" href="#">Pengaturan</a>
                <a class="dropdown-item" href="#">Keluar</a>
              </div>
            </li>
          </ul>
        </div>
      </nav>

    </div>
  </div>
</template>

<script>
import { Icon } from '@iconify/vue2'

export default {

  name: 'mainHeader',

  components:{
    Icon,
  },

  data () {
    return {

    }
  }
}
</script>

<style lang="css" scoped>
</style>