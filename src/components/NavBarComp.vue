<template>
  <nav>
    <ul class="flex px-10 sm:px-20 text-2xl whitespace-nowrap gap-10 overflow-x-scroll">
      <li class="transition duration-300 transform hover:scale-125 hover:text-white active:text-red-500" v-for="(title, i) of genreList" :key="i">
        <button>{{ title }}</button>
      </li>
    </ul>
  </nav>
</template>

<script setup lang="ts">
import requests from '@/utils/request'


let request = Object.entries(requests);
const genreList : String[] = [];

request.forEach(([key, {title, url}])=>{
  genreList.push(title);
})

</script>
