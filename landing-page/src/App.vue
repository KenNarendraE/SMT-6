<script setup>
  const items = ["Home",'Tentang Kita','Blog','Kontak']

const features = [


  {
    icon: "./src/icon/briefcase.svg",
    title: "Keseimbangan Kehidupan-Kerja",
    description:
      "Banyak pekerjaan jarak jauh dengan jadwal yang fleksibel, yang berarti bahwa para pekerja dapat memulai dan mengakhiri hari mereka sesuai keinginan.",
    color: "bg-orange",
  },

  {
    icon: "./src/icon/location.svg",
    title: "Bekerja Dimana Saja",
    description:
      "Memiliki akses ke peluang kerja yang lebih luas yang tidak dibatasi oleh lokasi geografis. Ini bisa sangat membantu.",
    color: "bg-blue",
  },

  {
    icon: "./src/icon/location.svg",
    title: "Peningkatan Inklusivitas",
    description:
      "Pekerjaan jarak jauh memungkinkan perusahaan untuk merangkul keragaman dan inklusi dengan mempekerjakan orang-orang dari latar belakang yang berbeda.",
    color: "bg-pink",
  },
];
</script>
<template>
  <div class="w-full min-h-screen font-sans text-gray-900">
    <div class="bg-gradient-to-b from-[#FEE6F7] to-white">
      <img src="/image/blob.svg" alt="" class="absolute top-0 right-0 pointer-events-none">
    <div class="px-6 mx-auto max-w-6xl">
      <div class="flex justify-between items-center py-10">
        <img src="./icon/logo.svg" alt="">
        <nav class="hidden md:flex md:items-center md:space-x-10">
          <a v-for="item in items" :key="item" class="text-gray-700 hover:text-gray-900" href="#">{{item}}</a>
          <a href="#" class="font-semibold text-green-600 hover:text-indigo-800">Try now</a>
        </nav>
        <button class="p-4 md:hidden">
          <img src="./icon/menu.svg" class="w-6 h-6 text-gray-800">
        </button> 
      </div>
      </div>
    </div>
      <div class="px-6 mx-auto max-w-6xl">
        <div class="flex flex-col-reverse items-center md:flex-row lg:items-end">
          <div class="pt-24 pr-8 pb-24 text-center md:pb-12 md:w-1/2 md:text-left">
            <h1 class="relative z-10 text-6xl font-bold font-display">
              Pelajari cara
              <span class="relative after:content-[url(/image/scratch.svg)] after:absolute after:-top-2 after:-right-6 after:-z-1">
              terbaik
              </span>
               untuk
              <span class="relative after:content-[url(/img/decoration.svg)] after:absolute after:-bottom-2 after:-right-8 after:-z-1">tetap</span>
               produktif
            </h1>
            <p class="pt-8 md:max-w-md text-xl leading-relaxed text-gray-500 md:text-xl">
              Bekerja di Rumah merupakan pilihan yang nyaman dan masuk akal di masa-masa yang belum pernah terjadi sebelumnya.
            </p>
            <div class="flex justify-center md:justify-start items-center pt-12 space-x-6">
              <button class="flex justify-center items-center py-4 px-8 font-bold tracking-wide leading-7 text-white bg-green-600 rounded-xl hover:shadow-xl">Dapatkan tips</button>
              <button class="flex items-center">
                <img src="./icon/play-button.svg" class="drop-shadow-lg hover:drop-shadow-xl">
                <span class="pl-4 font-bold tracking-wide">Pelajari Lagi</span>
              </button>
            </div>
          </div>
          <div class="w-1/2 flex items-end border-b border-gray-400">
            <img src="/image/illustration.svg" alt="">
          </div>
        </div>
      </div>
      <div class="bg-gray-50">
        <div class="py-12 px-6 mx-auto max-w-6xl">
          <div class="flex flex-col md:flex-row gap-x-5">
            <div v-for="feature in features" :key="feature" 
            class="flex flex-col p-8 space-y-4 bg-white rounded-lg border border-gray-200 hover:shadow-xl cursor-pointer transation-shadow duration-500 ease-out">
              <div class="flex items-center space-x-3">
                <div class="relative">
                <span :class="feature.color" class="absolute top-0 left-4 w-3 h-3 rounded-full opacity-50">
                  
                </span>
                <img v-bind:src="feature.icon"/>
                </div>
                <div class="relative">
                  <span :class="feature.color" class="absolute right-0 bottom-1 w-12 h-1.5 opacity-60"/>
                  <h2 class="text-xl font-display">{{feature.title}}</h2>
                </div>
              </div>
              <p class="text-sm leading-relaxed text-gray-500">{{feature.description}}</p>
            </div>
          </div>
        </div>
      </div>
  </div>
</template>