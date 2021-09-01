<template>
  <div class="bg-white shadow sticky-top">
    <div class="container">

      <nav class="navbar navbar-expand-lg navbar-light bg-transparent px-0">
        <a class="navbar-brand" href="/"><img src="~/static/img/logo.png" width="67px"></a>
        <!-- <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button> -->

        <div class="ml-auto" id="navbarSupportedContent">
          <ul class="navbar-nav flex-row ml-auto gap-3">
            <li class="nav-item">
              <a class="nav-link position-relative" href="/notifications">
                <Icon icon="clarity:notification-solid" style="font-size: 24px;" />
                <span class="position-absolute start-50 translate-middle p-1 bg-danger border border-danger rounded-circle mx-2 my-1">
                  <span class="visually-hidden">New alerts</span>
                </span>
              </a>
            </li>
            <li class="nav-item dropdown d-none d-lg-inline-block">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                <Icon icon="ci:settings-filled" style="font-size: 24px;"/>
              </a>
              <div class="dropdown-menu dropdown-menu-right" aria-labelledby="navbarDropdown">
                <a class="dropdown-item" href="/settings">Pengaturan</a>
                <a class="dropdown-item" href="#">Keluar</a>
              </div>
            </li>
            <li class="nav-item d-inline-block d-lg-none">
              <a class="nav-link position-relative" href="#" @click="openSidebar()">
                <Icon icon="heroicons-solid:menu-alt-3" style="font-size: 24px;" />
              </a>
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
  },
  methods: {
    openSidebar() {
      // console.log('clicked')
      this.$emit('sidebar')
    }
  }

}
</script>

<style lang="css" scoped>
</style>