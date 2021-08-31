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
                  <h5 class="mb-0">Draf</h5>
                  <ul class="navbar-nav flex-row gap-3 ml-auto">
                    <li class="nav-item">
                      <a class="nav-link text-secondary" href="#"><Icon icon="fontisto:spinner-refresh" style="font-size: 24px;" /></a>
                    </li>
                    <li class="nav-item dropdown">
                      <a class="nav-link text-secondary" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                        <Icon icon="fa-solid:sort-amount-up-alt" style="font-size: 24px;"/>
                      </a>
                      <div class="dropdown-menu dropdown-menu-right" aria-labelledby="navbarDropdown">
                        <a class="dropdown-item" href="#">Terbaru</a>
                        <a class="dropdown-item" href="#">Lama</a>
                      </div>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
            <div class="main-content py-4">
              <Thread />
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

export default {

  name: 'draft',

  components:{
    Sidebar,
    Icon
  },

  data () {
    return {

    }
  }
}
</script>

<style lang="css" scoped>
</style>