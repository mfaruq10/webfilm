<template>
    <div class="details">
            <div class="container">
              <div class="row detail-mov">
                <div class="col-md-12" v-for="(movie, index) in movies" :key="index">
                  <div v-if="proId == movie.id">
                    <h1>{{ movie.title }}</h1>
                    <img :src="movie.image" class="img-thumbnail">
                    <div class="a">
                      <span class="badge badge-pill badge-success margin-pill">{{ movie.duration }}</span>
                    </div>
                      <p class="content">Released Year : {{movie.release}}</p>
                    <p class="desc">{{movie.desc}}</p>
                  </div>
                </div>
              </div>
              <div class="button-area btn-lg">
                    <router-link to="/">Go back </router-link>
              </div>
            </div>
            <!-- <h1>id : {{ this.$route.params.Pid }}</h1> -->
    </div>
</template>
<script>
export default {
  name: 'detail',
  data () {
    return {
      proId: this.$route.params.Pid,
      title: 'Detail',
      movies: [
        {
          title: 'Dua Garis Biru',
          image: require('../assets/milea.jpg'),
          duration: '113 min',
          director: 'Gina S. Noer',
          release: 2019,
          desc: 'Bima dan Dara adalah sepasang kekasih yang masih duduk di bangku SMA. Bima memiliki nilai akademis yang rendah, dan itu sebaliknya bagi Dara. Mereka sangatlah mencintai sesama dan sering bermain bersama, hingga suatu saat, mereka melampaui batas dengan cara bersetubuh diluar nikah. Setelah kejadian itu, Bima dan Dara tidak berbicara satu sama lain, hingga suatu saat, ketika Dara dikonfirmasi hamil. Mengetahui apa yang terjadi, Bima ingin mencoba mengatakannya kepada orangtuanya, namun tidak mampu.',
          id: 1
        },
        {
          title: 'Tersanjung',
          image: require('../assets/tersanjung.jpg'),
          duration: '130 min',
          director: 'Hanung',
          release: 2011,
          desc: 'Di tahun 90-an, masa di saat tokoh-tokoh di ujung transisi menuju milenium baru. Yura (Clara Bernadeth) gadis malang yang tinggal dengan orang tua angkat, dibuai oleh harapan jatuh ke pelukan keluarga kaya. Tapi malang tak bisa ditolak, Yura yang sempat tersanjung, mengecap harapan sesaat, mesti dicampakkan.',
          id: 2
        },
        {
          title: 'Toko Barang Mantan',
          image: require('../assets/tokomantan.jpg'),
          duration: '142 min',
          director: 'Mas Ali',
          release: 2020,
          desc: 'Toko Barang Mantan adalah toko jual-beli barang-barang mantan bagi orang-orang yang ingin move-on dari mantannya. Sebagai pencetus ide, pendiri dan pemiliknya, Tristan rela meninggalkan kuliah hukumnya demi bisa fokus mengembangkan toko ini bersama sahabatnya, Amel dan Rio. Berbagai macam kisah-kisah sedih, lucu dan absurd tentang barang-barang tersebut menjadi makanan mereka sehari-hari.',
          id: 3
        },
        {
          title: 'Mariposa',
          image: require('../assets/mariposa.jpg'),
          duration: '102 min',
          director: 'Brian Fee',
          release: 2020,
          desc: 'Mariposa (Kupu-kupu) seperti kamu, aku mengejar tapi kamu menghindar. Begitulah gambaran sosok IQBAL GUANNA bagi NATASHA KAY LOOVY atau ACHA. Acha bertekad ingin mendapatkan hati Iqbal, seorang cowok cakep, pintar dan dikenal berhati dingin. Sahabat Acha, AMANDA, berusaha mencegah niat Acha untuk mendekati Iqbal. Amanda takut Acha akan terluka dan sakit hati.',
          id: 4
        }
      ]
    }
  }
}
</script>
<style>
  .detail-mov
  {
    text-align: center
    
  }
  .a
  {
    margin-top: 10px;
  }
  .desc
  {
    text-align: left;
  }
  p, h1, h2, h3, h4
  {
    color: black;
  }
</style>
