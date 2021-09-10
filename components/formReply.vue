<template>
  <div id="formReply" :class="{ 'open': reply }">
    <div class="position-relative mb-4 d-block d-lg-none">
      <a class="text-secondary position-absolute start-0" @click="closeReply()"><Icon icon="eva:arrow-back-outline" style="font-size: 24px;"/></a>
      <h5 class="m-0 w-100 text-center">Berikan Jawaban</h5>
    </div>
    <div class="card p-0 p-lg-3 mb-3">
      <b-form-textarea id="textarea" v-model="text" placeholder="Tulis disini..." rows="3" max-rows="6" class="mb-3 border-0 p-0 bg-transparent"></b-form-textarea>
      <div class="d-grid gap-2 fileUpload">
        <div class="card bg-light border-0">
          <div class="card-body p-3">
            <div class="d-flex align-items-center justify-content-between">
              <div class="card-text">gambarlumut.jpeg <span class="text-light">(15mb)</span></div>
              <div class="d-flex align-items-center gap-3">
                <nuxt-link to="" class="text-dark"><Icon icon="eva:close-fill" style="font-size: 24px;"/></nuxt-link>
              </div>
            </div>
          </div>
        </div>
        <div class="card bg-light border-0">
          <div class="card-body p-3">
            <div class="d-flex align-items-center justify-content-between">
              <div class="card-text">gambarlumut.jpeg <span class="text-light">(15mb)</span></div>
              <div class="d-flex align-items-center gap-3">
                <div class="progress">
                  <div class="progress-bar bg-secondary rounded-pill" role="progressbar" style="width: 50%" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"></div>
                </div>
                <nuxt-link to="" class="text-danger">Batalkan</nuxt-link>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="cta d-flex align-items-center justify-content-end gap-1">
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

  name: 'formReply',

  props: {
    reply: Boolean
  },

  components:{
    Icon,
  },

  data () {
    return {
      text: ''
    } 
  },

  methods: {
    closeReply() {
      // console.log('clicked')
      this.$emit('reply')
    }
  }
}
</script>

<style lang="scss" scoped>
.progress{
  height: 10px;
  width: 150px;
}
@media (max-width: 767px){
  .cta{
    position: fixed;
    bottom: 0;
    width: 90%;
    border-top: 1px solid #ddd;
    padding: 15px 0;
  }
}
</style>