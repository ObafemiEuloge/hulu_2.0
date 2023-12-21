<template>
  <header class="flex flex-col-reverse sm:flex-row m-5 justify-between items-center">
    <ul class="flex flex-grow gap-4 sm:gap-0 justify-evenly max-w-2xl">
      <HeaderItem v-for="(link, i) of links" :title="link.title" :Icon="link.icon" :key="i" />
    </ul>
    <div>
      <img src="/asset/hululogo.webp" alt="" />
    </div>
  </header>
</template>

<script setup lang="ts">
import HeaderItem from "@/components/HeaderItem.vue";
import {HomeIcon, BoltIcon, CheckBadgeIcon, RectangleStackIcon, MagnifyingGlassIcon, UserIcon} from "@heroicons/vue/24/outline";

const links = [
  {title: "Home", icon: HomeIcon},
  {title: "Trending", icon: BoltIcon},
  {title: "Verified", icon: CheckBadgeIcon},
  {title: "Collections", icon: RectangleStackIcon},
  {title: "Search", icon: MagnifyingGlassIcon},
  {title: "Account", icon: UserIcon},
]
</script>

