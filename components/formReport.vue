<template>
  <div>
    <b-form-textarea id="textarea" v-model="text" placeholder="Tulis disini..." rows="3" max-rows="6" class="mb-3"></b-form-textarea>
    <div class="d-flex align-items-center justify-content-end gap-1">
      <div class="d-flex"> 
        <nuxt-link to="" class="btn btn-outline-secondary border-0"><Icon icon="bi:file-earmark-image-fill" style="font-size: 24px;"/></nuxt-link>
        <nuxt-link to="" class="btn btn-outline-secondary border-0"><Icon icon="eva:attach-2-outline" style="font-size: 24px;"/></nuxt-link>
        <nuxt-link to="" class="btn btn-outline-secondary border-0"><Icon icon="bi:file-earmark-fill" style="font-size: 24px;"/></nuxt-link>
      </div>
      <nuxt-link to="" class="btn btn-success px-5">Kirim</nuxt-link>
    </div>
  </div>
</template>

<script>
import { Icon } from '@iconify/vue2';

export default {

  name: 'formReport',

  components:{
    Icon,
  },

  data () {
    return {
      text: ''
    } 
  }
}
</script>

<style lang="css" scoped>
</style>