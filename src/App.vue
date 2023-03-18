<script setup>

import Navbar from "./components/partials/Navbar.vue"
import { ref } from "vue"

const dataA = ref(0)
const dataB = ref(0)
const nama =  ref("")
const pesan =  ref("")

const noActive = 'w-full bg-emerald-500 text-white rounded-md px-10 py-2 shadow-md hover:bg-emerald-600'
const active ='border-2 border-white'


</script>

<template>
  <div>
    <Navbar />

    <section class=" bg-gradient-to-b from-emerald-200 to-white">
      <div class="container mx-auto px-6 sm:px-10 md:px-12 lg:px-16 py-16">
        <div class="md:flex justify-between space-y-10 md:space-y-0 items-center">
          <div class="lg:w-1/2">
            <div>
              <h3 class="text-lg md:text-xl text-emerald-600 font-bold">Hallo, selamat datang</h3>
              <h3 class="text-2xl md:text-3xl font-bold">Menjaga Kesehatan Pada Bumi Kita</h3>
              <p>Ayo! lakukan sekarang, kalo bukan kita siapa lagi!</p>
            </div>
            <a href="/#lainya" class="w-fit mt-5 block px-10 py-2 rounded-md shadow text-white bg-blue-600 text-center">Baca Lainya</a>
          </div>
          <div>
            <img src="./assets/img-1.png" class="w-72 mx-auto" alt="">
          </div>
        </div>
      </div>
    </section>

    <section id="lainya">
      <div class="container mx-auto px-6 sm:px-10 md:px-12 lg:px-16 py-16">
        <div class="mb-10">
          <h3 class="text-2xl md:text-3xl font-bold">Mengapa Harus Menjaga Bumi ?</h3>
          <h3 class="text-xl md:text-2xl font-bold text-gray-400">Apa alasanya ?</h3>
        </div>
        <div class="px-3 py-5 rounded-md shadow-md md:flex justify-around items-center space-y-5 md:space-y-0 bg-emerald-400">
          <div class="md:w-1/2">
            <h3 class="font-bold text-lg">Alasan Pertama</h3>
            <p class="text-white">Kepedulian terhadap lingkungan harus ditunjukkan setiap orang. Hal ini perlu dilakukan untuk menjaga keberlangsungan hidup manusia, hewan, tumbuhan. Jika tidak dirawat dengan baik, akan terjadi kerusakan pada alam dan bisa mengancam setiap makhluk hidup</p>
          </div>
          <div>
            <img src="./assets/img-2.png" class="w-56 mx-auto" alt="">
          </div>
        </div>
        <div class="px-3 py-5 rounded-md shadow-md md:flex justify-around items-center space-y-5 md:space-y-0 mt-5 bg-emerald-400">
          <div>
            <img src="./assets/img-3.png" class="w-56 mx-auto" alt="">
          </div>
          <div class="md:w-1/2 md:text-right">
            <h3 class="font-bold text-lg">Alasan Kedua</h3>
            <p class="text-white">Sebab dari lingkungan yang kita tinggali, kita bisa memenuhi segala kebutuhan sehari-hari. Jika manusia hanya memanfaatkannya tanpa melestarikan, maka lingkungan bisa menjadi rusak. Dampak dari kerusakan lingkungan nantinya akan dirasakan oleh manusia sendiri, bahkan juga makhluk hidup lain.</p>
          </div>
        </div>
      </div>
    </section>

    <section class=" bg-emerald-100">
      <div class="container mx-auto px-6 sm:px-10 md:px-12 lg:px-16 py-16">
        <div class="mb-10">
          <h3 class="text-2xl md:text-3xl font-bold">Apakah Kalian Sudah Tahu ?</h3>
          <h3 class="text-xl md:text-2xl font-bold text-gray-400">Hal hal dibawah ini dapat merusak bumi loh..</h3>
        </div>
        <div class="md:flex justify-between gap-x-10 space-y-5 md:space-y-0 items-center">
          <div class="space-y-3 md:w-1/2">
            <button :class="dataA == 1 ? [noActive, active] : [noActive]" @click="dataA = 1">Membuang sampah sembarangan</button>
            <button :class="dataA == 2 ? [noActive, active] : [noActive]" @click="dataA = 2">Menggunakan pendingin ruangan</button>
            <button :class="dataA == 3 ? [noActive, active] : [noActive]" @click="dataA = 3">Pemborosan listrik</button>
            <p class="text-sm text-center">( Tekan tombol untuk mengetahui penjelasan nya )</p>
            <div class="mt-5 rounded-md border-2 border-emerald-500 px-5 py-3" v-if="dataA == 1">
              Dampak membuang sampah sembarangan akan merusak pemandangan, mendatangkan bau yang tidak sedap, mendatangkan banjir level rendah sampai yang tinggi, mendatangkan berbagai penyakit dan dapat mencemari lingkungan.
            </div>
            <div class="mt-5 rounded-md border-2 border-emerald-500 px-5 py-3" v-if="dataA == 2">
              Mengapa penggunaan AC dapat meningkatkan pemanasan di muka bumi? Hal tersebut dikarenakan AC menggunakan gas CFC (salah satu gas rumah kaca) yang dapat merusak lapisan ozon bumi.
            </div>
            <div class="mt-5 rounded-md border-2 border-emerald-500 px-5 py-3" v-if="dataA == 3">
              Dampak Buruk Penggunaan Listrik Secara Berlebihan. Terjadinya peningkatan suhu global akibat dari panasnya energi listrik yang terlalu lama digunakan atau penggunaannya melebihi batas. Pemborosan energi listrik juga dapat menyebabkan kemungkinan cuaca ekstrim di suatu wilayah tertentu.
            </div>
            <button @click="dataA = 0" v-if="dataA != 0" class="bg-red-500 text-white rounded-md shadow px-5 py-2 text-sm">Tutup Penjelasan</button>
          </div>
          <div>
            <img src="./assets/img-4.png" class="mx-auto  w-56 sm:w-62 md:w-68 lg:w-72" alt="">
          </div>
        </div>
      </div>
    </section>
    <section class="bg-emerald-100">
      <div class="container mx-auto px-6 sm:px-10 md:px-12 lg:px-16 py-16">
        <div class="mb-10 md:text-right">
          <h3 class="text-2xl md:text-3xl font-bold">Hal Hal Yang Harus Kita Lakukan</h3>
          <h3 class="text-xl md:text-2xl font-bold text-gray-400">Beberapa contoh menjaga kesehatan bumi</h3>
        </div>
        <div class="md:flex justify-between gap-x-10 space-y-5 md:space-y-0 items-center">
          <div>
            <img src="./assets/img-5.png" class="mx-auto w-56 sm:w-62 md:w-68 lg:w-72" alt="">
          </div>
          <div class="space-y-3 md:w-1/2">
            <button :class="dataB == 1 ? [noActive, active] : [noActive]" @click="dataB = 1">Menanam pohon</button>
            <button :class="dataB == 2 ? [noActive, active] : [noActive]" @click="dataB = 2">Tidak mengganggu ekosistem</button>
            <button :class="dataB == 3 ? [noActive, active] : [noActive]" @click="dataB = 3">Melakukan daur ulang</button>
            <p class="text-sm text-center">( Tekan tombol untuk mengetahui penjelasan nya )</p>
            <div class="mt-5 rounded-md border-2 border-emerald-500 px-5 py-3" v-if="dataB == 1">
              Pohon adalah penyaring udara dan air tanah yang alami. Pohon dapat meningkatkan kualitas udara dan air tanah, dua hal vital yang diperlukan oleh semua makhluk hidup.
            </div>
            <div class="mt-5 rounded-md border-2 border-emerald-500 px-5 py-3" v-if="dataB == 2">
              Semua yang ada di Bumi kita ini memiliki fungsi yang saling menunjang satu sama lain. Hewan-hewan dengan satu dan berbagai cara membantu penyebaran bibit tanaman dan hutan pun terjaga kelestariannya.
            </div>
            <div class="mt-5 rounded-md border-2 border-emerald-500 px-5 py-3" v-if="dataB == 3">
              Pengepul sampah adalah partner yang bisa membantu Anda mendaur ulang, begitupun dengan Bank Sampah yang saat ini sudah ada di berbagai wilayah. Tanyakan ke pengurus warga, di mana alamat Bank Sampah yang terdekat dengan tempat tinggal Anda.
            </div>
            <button @click="dataB = 0" v-if="dataB != 0" class="bg-red-500 text-white rounded-md shadow px-5 py-2 text-sm">Tutup Penjelasan</button>
          </div>
        </div>
      </div>
    </section>
    <section class="container mx-auto px-6 sm:px-10 md:px-12 lg:px-16 py-16">
      <div>
        <div class="mb-10 text-center">
          <h3 class="text-2xl md:text-3xl font-bold">Hal Hal Yang Harus Kita Lakukan</h3>
          <div class="flex justify-center items-center gap-x-5 mt-5">
            <div class="h-5 w-5 rounded-full bg-emerald-500"></div>
            <div class="h-5 w-5 rounded-full bg-emerald-500"></div>
            <div class="h-5 w-5 rounded-full bg-emerald-500"></div>
          </div>
        </div>
      </div>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-x-5 gap-y-5 lg:gap-y-0">
        <div>
          <h3 class="font-bold text-xl mb-3 md:text-2xl text-center">Polusi Udara</h3>
          <img src="./assets/img-6.png" class="w-56 rounded-md shadow-md mx-auto h-56" alt="">
          <p class="text-center mt-3">Tahukah kamu bahwa udara yang tercemar bisa mempengaruhi umur kamu? Udara yang dipenuhi dengan asap serta karsinogen bisa membunuh atau memperpendek usia kamu lebih cepat dibandingkan saat kamu sedang merokok.</p>
        </div>
        <div>
          <h3 class="font-bold text-xl mb-3 md:text-2xl text-center">Polusi Udara</h3>
          <img src="./assets/img-7.png" class="w-56 rounded-md shadow-md mx-auto h-56" alt="">
          <p class="text-center mt-3">Air yang terkontaminasi oleh racun juga bisa mengganggu kualitas hidupmu. Tak hanya membahayakan untuk manusia, air yang terkontaminasi limbah beracun juga bisa membahayakan kesehatan hewan.</p>
        </div>
        <div>
          <h3 class="font-bold text-xl mb-3 md:text-2xl text-center">Polusi Udara</h3>
          <img src="./assets/img-8.png" class="w-56 rounded-md shadow-md mx-auto h-56" alt="">
          <p class="text-center mt-3">Penggunaan kendaraan dalam jumlah yang banyak senantiasa terus meningkat saat ini. Hasilnya, tak hanya polusi udara yang makin bertambah, pemanasan global juga terjadi yang membuat bumi semakin bertambah panas.</p>
        </div>
      </div>
    </section>

    <section class=" bg-emerald-600">
      <div class="container mx-auto px-6 sm:px-10 md:px-12 lg:px-16 py-16">
        <div class="text-center">
          <h3 class="font-bold text-2xl md:text-3xl">Berikan Masukan</h3>
        </div>
        <div class="flex justify-center mt-20">
          <div class="space-y-3">
            <div>
              <label for="name" class="block w-fit text-lg font-bold">Nama</label>
              <input id="name" v-model="nama" placeholder="Nama anda" type="text" class="w-full px-5 py-2 rounded-md shadow bg-gray-200 focus:outline-emerald-400 focus:outline-offset-1">
            </div>
            <div>
              <label for="pesan" class="block w-fit text-lg font-bold">Pesan</label>
              <textarea id="pesan" v-model="pesan" placeholder="Masukan anda" type="text" class="w-full px-5 py-2 rounded-md shadow bg-gray-200 focus:outline-emerald-400 focus:outline-offset-1" cols="15" rows="5"></textarea>
            </div>
            <a :href="`https://wa.me/6289601648595?text=Hallo, nama saya ${nama}. Pesan saya adalah ${pesan}`" class="block w-full bg-sky-600 hover:bg-sky-700 text-center text-white rounded-md shadow-md px-10 py-2">Submit</a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>