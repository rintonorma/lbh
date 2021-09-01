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
                  <h5 class="mb-0">Notifikasi</h5>
                  <ul class="navbar-nav flex-row gap-3 ml-auto">
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
                <div class="d-flex gap-3 py-3 border-bottom" v-for="item in notif" :key="item.id">
                  <div class="avatar avatar-lg flex-shrink-0">
                    <img :src="item.src" class="card-img-top">
                  </div>
                  <div class="d-grid gap-2 w-100">
                    <div class="d-flex align-items-center justify-content-between w-100">
                      <div class="d-flex align-items-center gap-2">
                        <div class="text-danger">{{ item.object }}</div>
                        <div class="text-secondary"><small>{{ item.subject }}</small></div>
                      </div>
                      <ul class="navbar-nav">
                        <li class="nav-item dropdown">
                          <a class="nav-link p-0 text-secondary" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                            <Icon icon="octicon:kebab-horizontal-24" style="font-size: 24px;"/>
                          </a>
                          <div class="dropdown-menu dropdown-menu-right" aria-labelledby="navbarDropdown">
                            <a class="dropdown-item" href="#">Hapus</a>
                          </div>
                        </li>
                      </ul>
                    </div>
                    <div class="elipsis-1">{{ item.content }}</div>
                    <div class="text-secondary"><small>{{ item.datetime }}</small></div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <Sidebar :open="open" @sidebar="openSidebar" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Sidebar from '~/components/sidebar'
import { Icon } from '@iconify/vue2'

export default {

  name: 'notifications',

  components:{
    Sidebar,
    Icon
  },

  data () {
    return {
      open: false,
      notif:[
        {
          id: 1,
          src: '/img/logo.png',
          object: 'LBH HKTI',
          subject: 'Menjawab laporan Anda',
          content: 'kpd yth bpk/ibu ditempat saya ingin bertanya bagaimana cara untuk mengirimkan laporan dengan benar',
          datetime: '13 Agu 2021 16:56'
        },
        {
          id: 2,
          src: '/img/logo.png',
          object: 'LBH HKTI',
          subject: 'Menjawab laporan Anda',
          content: 'kpd yth bpk/ibu ditempat saya ingin bertanya bagaimana cara untuk mengirimkan laporan dengan benar',
          datetime: '13 Agu 2021 16:56'
        },
        {
          id: 3,
          src: '/img/logo.png',
          object: 'LBH HKTI',
          subject: 'Menjawab laporan Anda',
          content: 'kpd yth bpk/ibu ditempat saya ingin bertanya bagaimana cara untuk mengirimkan laporan dengan benar',
          datetime: '13 Agu 2021 16:56'
        },
      ],
    }
  },

  methods: {
    openSidebar() {
      this.open = ! this.open
    }
  }
}
</script>

<style lang="scss" scoped>
.elipsis-1{
  display: block;
  display: -webkit-box;
  max-width: 100%;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: normal;
}
</style>