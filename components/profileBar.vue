<template>
  <div class="d-flex align-items-center gap-2">
    <div class="position-relative">
      <div class="avatar avatar-xl">
        <img src="~/static/img/photo-1519993796861-26556330a4a9.jpeg">
      </div>
      <div class="position-absolute end-0 bottom-0">
        <nuxt-link to="" class="d-flex bg-white rounded-pill text-dark shadow p-2"><Icon icon="ant-design:camera-filled" style="font-size: 18px;" class=""/></nuxt-link>
      </div>
    </div>
    <div class="d-grid gap-2">
      <div class="d-flex align-items-center gap-2">
        <h5 class="m-0">Budiman Mulianto</h5>
        <Icon icon="bi:check-circle-fill" style="font-size: 18px;" class="text-primary"/>
      </div>
      <div class="d-flex align-items-center gap-2">
        <Icon icon="ci:location" style="font-size: 18px;" class="text-danger"/>
        Kab. Majalengka
      </div>
    </div>
  </div>
</template>

<script>
import { Icon } from '@iconify/vue2'

export default {

  name: 'profileBar',

  components:{
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