<script setup lang="ts">
import Vue from './assets/vue.png'
import Vite from './assets/vitejs.png'
import WindiCSS from './assets/windicss.png'
import Directions from './assets/directions.svg'
import Package from './assets/package.svg'
import Card from './components/Card.vue';
</script>

<template>
  <div class="flex h-screen bg-light-200 justify-center items-center">
    <div class="flex flex-col w-2/3 justify-center items-center">
      <img v-bind:src="Vue" alt="Vue" class="h-auto w-40" />
      <h1 class="font-semibold mt-5 text-2xl">
        Approachable, performant, and versatile
      </h1>
      <h1 class="font-light text-xl text-gray-500">For the love of ease</h1>
      <div class="mt-10 grid gap-3 grid-cols-2">
        <Card title="Vite" v-bind:icon="Vite"
          body="A build tool that aims to provide a faster and leaner development experience for modern web projects."
          url="https://vitejs.dev" />
        <Card title="WindiCSS" v-bind:icon="WindiCSS"
          body="Next generation utility-first CSS framework. It's easy to use and wicked fast."
          url="https://windicss.org" />
        <Card title="Vue Router" v-bind:icon="Directions"
          body="You're going to need some way to navigate your app. And thats what this guy is here to do."
          url="https://router.vuejs.org/#direct-download-cdn" />
        <Card title="Oh Vue Icons" v-bind:icon="Package"
          body="Inclue inline SVG icons from several popular icon packs with ease."
          url="https://oh-vue-icons.netlify.app/" />
        <Card lg title="Vue" v-bind:icon="Vue"
          body="Vue is the Progressive JavaScript Framework. It's approachable, performant, and versatile. Thats why its perferct for your project. Whatever you need Vue will have you covered."
          url="https://vuejs.org" />
      </div>
    </div>
  </div>
</template>
