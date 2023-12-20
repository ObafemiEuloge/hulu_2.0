<template>
    <li class="flex flex-col cursor-pointer hover:text-white transition-all duration-500 group">
        <Icon class="h-8 mb-1 group-hover:animate-bounce transition-all duration-500"/>
        <a href="#" class="uppercase">{{title}}</a>
    </li>
</template>

<script setup lang="ts">
import type { FunctionalComponent, HTMLAttributes, VNodeProps } from 'vue';

    const props = defineProps<{
        title : String,
        Icon : FunctionalComponent<HTMLAttributes & VNodeProps, any>,
    }>();
</script>
