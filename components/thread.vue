<template>
  <div>
    <!-- tanpa jawaban -->
    <div class="card mb-4">
      <div class="card-header bg-transparent border-0">
        <div class="d-flex align-items-center justify-content-between">
          <div class="d-flex align-items-center gap-2">
            <div class="avatar avatar-lg">
              <img src="~/static/img/photo-1519993796861-26556330a4a9.jpeg">
            </div>
            <div class="d-grid">
              <div class="m-0">Budiman Mulianto</div>
              <div class="text-light"><small>13 Agu 2021 16:56</small></div>
            </div>
          </div>
          <div>
            <div class="dropdown">
              <button class="btn btn-outline-secondary border-0" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                <Icon icon="octicon:kebab-horizontal-24" style="font-size: 24px;"/>
              </button>
              <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
                <a class="dropdown-item" href="#">Hapus</a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="card-body">
        <div class="main-content">
          Ketika berjalan tanpa alas kaki di hutan, mungkin Anda pernah merasakan lumut yang lembut dan licin di telapak kaki. Lumut sangat cocok ditempatkan di halaman dan kebun karena bisa menjaga kelembapan dan tidak perlu dipangkas seperti rumput. Anda juga bisa menyebarkan lumut pada pagar, fondasi, atau batu untuk memberi nuansa hutan. Untuk menanam lumut, Anda hanya perlu sedikit bersusah-payah di saat awal, lalu membiarkannya tumbuh sendiri dan hidup hingga bertahun-tahun.
        </div>
        <hr>
        <div class="row">
          <div class="col-6 col-lg-4 mb-4" v-for="i in 4" :key="i">
            <nuxt-link to="" class="card hover-download">
              <div class="ratio ratio-21x9">
                <div class="overlay card-img-top"><Icon icon="bx:bxs-download" style="font-size: 24px;"/></div>
                <img src="~/static/img/agriculture-countryside-crop-cropland-388415.jpg" class="card-img-top" alt="...">
              </div>
              <div class="card-footer d-flex align-items-center justify-content-between border-0 overflow-hidden p-0">
                <div class="card-text px-2">tanaman-pandan-ijo</div>
                <div class="bg-danger text-white p-2">Jpeg</div>
              </div>
            </nuxt-link>
          </div>
        </div>
        <div class="d-flex align-items-center justify-content-end gap-2">
          <Icon icon="ic:baseline-question-answer" style="font-size: 24px;" class="text-secondary"/>
          <div>1 Jawaban</div>
        </div>
      </div>
    </div>

    <!-- dengan jawaban -->
    <div class="card mb-4">
      <div class="card-header bg-transparent border-0">
        <div class="d-flex align-items-center justify-content-between">
          <div class="d-flex align-items-center gap-2">
            <div class="avatar avatar-lg">
              <img src="~/static/img/photo-1519993796861-26556330a4a9.jpeg">
            </div>
            <div class="d-grid">
              <div class="m-0">Budiman Mulianto</div>
              <div class="text-light"><small>13 Agu 2021 16:56</small></div>
            </div>
          </div>
          <div>
            <div class="dropdown">
              <button class="btn btn-outline-secondary border-0" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                <Icon icon="octicon:kebab-horizontal-24" style="font-size: 24px;"/>
              </button>
              <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
                <a class="dropdown-item" href="#">Hapus</a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="card-body">
        <div class="main-content">
          Anda memerlukan tanah campuran, air, dan sinar matahari untuk menanam bibit atau pohon yang masih kecil. Kebutuhan tanaman terhadap suhu yang tepat, air, dan sinar matahari berbeda-beda. Selain mengikuti panduan yang dijelaskan di artikel ini, bacalah juga keterangan yang tercantum di tanaman dengan saksama agar Anda bisa memenuhi persyaratan tanaman dengan tepat. Anda bisa menjadi ahli menanam dengan mengikuti beberapa petunjuk mudah di bawah ini.
        </div>
        <hr>
        <div class="row">
          <div class="col-6 col-lg-4 mb-4" v-for="i in 4" :key="i">
            <nuxt-link to="" class="card hover-download">
              <div class="ratio ratio-21x9">
                <div class="overlay card-img-top"><Icon icon="bx:bxs-download" style="font-size: 24px;"/></div>
                <img src="~/static/img/agriculture-countryside-crop-cropland-388415.jpg" class="card-img-top" alt="...">
              </div>
              <div class="card-footer d-flex align-items-center justify-content-between border-0 overflow-hidden p-0">
                <div class="card-text px-2">tanaman-pandan-ijo</div>
                <div class="bg-danger text-white p-2">Jpeg</div>
              </div>
            </nuxt-link>
          </div>
        </div>
        <div class="d-flex align-items-center justify-content-end gap-2">
          <Icon icon="ic:baseline-question-answer" style="font-size: 24px;" class="text-secondary"/>
          <div>1 Jawaban</div>
        </div>
      </div>
      <div class="divider"></div>
      <div class="card-header bg-transparent border-0">
        <div class="d-flex align-items-center justify-content-between">
          <div class="d-flex align-items-center gap-2">
            <div class="avatar avatar-lg">
              <img src="~/static/img/logo.png">
            </div>
            <div class="d-grid">
              <div class="m-0">LBH HKTI</div>
              <div class="text-light"><small>13 Agu 2021 16:56</small></div>
            </div>
          </div>
          <div>
            <div class="dropdown">
              <button class="btn btn-outline-secondary border-0" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                <Icon icon="octicon:kebab-horizontal-24" style="font-size: 24px;"/>
              </button>
              <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
                <a class="dropdown-item" href="#">Laporkan</a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="card-body">
        <div class="main-content">
          Tentukan lokasi penanaman. Lokasi penanaman adalah hal yang sangat penting. Pastikan tempat yang dipilih mendapatkan sinar matahari dalam jumlah yang memadai, memiliki ruang yang mencukupi, tanah yang subur untuk pertumbuhan, dan drainase yang baik.[1] Hadapkan tanaman ke timur karena sinar matahari pagi merupakan sumber cahaya terbaik dan sejuk agar tanaman bisa tumbuh subur. Tanah harus gembur dan berwarna gelap, bukan merah dan banyak mengandung lempung atau pasir. Tanah yang gembur memiliki aerasi yang bagus sehingga akar bisa tumbuh dengan mudah, sedangkan warna yang gelap menunjukkan bahwa tanahnya sangat subur.
        </div>
        <div class="ratio ratio-16x9 my-3">
          <img src="~/static/img/agriculture-asia-china-235648.jpg" class="rounded">
        </div>
        <div class="d-flex align-items-center justify-content-end gap-2">
          <Icon icon="bi:reply-fill" style="font-size: 24px;" class="text-secondary"/>
          <div>Balas Jawaban</div>
        </div>
      </div>
      <div class="divider"></div>
      <div class="card-footer bg-transparent border-0">
        <FormReport />
      </div>
    </div>


  </div>
</template>

<script>
import { Icon } from '@iconify/vue2'
import FormReport from '~/components/formReport'

export default {

  name: 'thread',

  components:{
    Icon,
    FormReport
  },

  data () {
    return {

    }
  }
}
</script>

<style lang="scss" scoped>
.hover-download{
  color: #2A2B2A;

  &:hover{
    text-decoration: none;
  }
}
.hover-download .overlay{
  opacity: 0;
  transition: all ease 0.2s;
}
.hover-download:hover .overlay{
  opacity: 1;
}
</style>








