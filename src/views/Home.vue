<template>
<div id="home">
    <div class="container">
            <div class="row row-cols-4 ">
            <div class="col-xl-3 col-12" v-for="(data, index) in movies" :key="index">
                <div class="image-area">
                    <img :src="data.image" class="image">
                </div>
                <div class="content-area">
                    <h4 style="color:black;">{{ data.title}} ({{data.release}})</h4>
                    <span class="badge badge-pill badge-success margin-pill">{{ data.duration }}</span>
                    <p class="font-text">Dircted by : <b>{{ data.director }}</b></p>
                </div>
                <div class="button-area">
                    <button class="btn btn-info" @click="goToDetail(data.id)">Info</button>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      title: 'Home',
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
          director: ' Hanung Bramantyo',
          release: 2020,
          desc: 'Di tahun 90-an, masa di saat tokoh-tokoh di ujung transisi menuju milenium baru. Yura (Clara Bernadeth) gadis malang yang tinggal dengan orang tua angkat, dibuai oleh harapan jatuh ke pelukan keluarga kaya. Tapi malang tak bisa ditolak, Yura yang sempat tersanjung, mengecap harapan sesaat, mesti dicampakkan.',
          id: 2
        },
        {
          title: 'Barang Mantan',
          image: require('../assets/tokomantan.jpg'),
          duration: '142 min',
          director: 'Viva Westi',
          release: 2020,
          desc: 'Toko Barang Mantan adalah toko jual-beli barang-barang mantan bagi orang-orang yang ingin move-on dari mantannya. Sebagai pencetus ide, pendiri dan pemiliknya, Tristan rela meninggalkan kuliah hukumnya demi bisa fokus mengembangkan toko ini bersama sahabatnya, Amel dan Rio. Berbagai macam kisah-kisah sedih, lucu dan absurd tentang barang-barang tersebut menjadi makanan mereka sehari-hari.',
          id: 3
        },
        {
          title: 'Mariposa',
          image: require('../assets/mariposa.jpg'),
          duration: '102 min',
          director: 'Kusnandar',
          release: 2020,
          desc: 'Lightning McQueen sets out to prove to a new generation of racers that he is still the best race car in the world.',
          id: 4
        }
      ]
    }
  },
  methods: {
    goToDetail (proId) {
      this.$router.push({ name: 'detail', params: { Pid: proId } })
    }
  }
}

</script>

<style>
.container
{
    margin-top: 2%;
    margin: 50px;
}
.font-text
{
    font-size: 9pt;
    margin: 10px 0;
    color: black;
}
.image-area
{
    width: 200px;
    height: 300px;
    text-align: center;
}
.image{
    width: 200px;
    height: 300px;
}
.content-area
{
    margin: 10px 0;
    height: 30%;
    color: black;
}
</style>
