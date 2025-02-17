<script setup lang="ts">
import { Search } from 'lucide-vue-next';

</script>

<template>
    <div class="w-full relative">
        <input type="search" placeholder="Search..."
            class="w-full py-4 px-6 pr-20 rounded-md bg-[#2b2e33] shadow-md shadow-black/40 border-transparent transition-all focus:ring-2 focus:ring-[#eaeaea] focus:border-transparent text-white">
        <Search class="absolute top-1/2 -translate-y-1/2 right-6 text-[#eaeaea]" />
    </div>
</template>