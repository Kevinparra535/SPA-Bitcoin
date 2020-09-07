<template>
  <div class="flex-col items-center text-center">
    <lottie-player
      src="https://assets7.lottiefiles.com/packages/lf20_CiKDQB.json"
      background="transparent"
      speed="1"
      style="width: 100%; height: 300px;"
      loop
      autoplay
    ></lottie-player>
    <h1 class="text-gray-700 text-6xl uppercase">error</h1>
    <router-link
      class="mt-5 text-xl bg-purple-500 py-2 px-4 text-gray-100 hover:underline rounded-lg"
      to="/"
      >Volver a la página de Inicio</router-link
    >
  </div>
</template>
