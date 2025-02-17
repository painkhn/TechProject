<script setup lang="ts">
import { Image } from 'lucide-vue-next';
const projects = [
    {
        title: 'Example Title',
        description: 'Example Description',
        deadline: '30.02.2025',
        tags: [
            {
                name: 'Web'
            },
            {
                name: 'UX'
            },
        ]
    },
    {
        title: 'Example Title',
        description: 'Example Description',
        deadline: '30.02.2025',
        tags: [
            {
                name: 'Web'
            },
            {
                name: 'UX'
            },
        ]
    },
    {
        title: 'Example Title',
        description: 'Example Description',
        deadline: '30.02.2025',
        tags: [
            {
                name: 'Web'
            },
            {
                name: 'UX'
            },
        ]
    }
]

import ContentBlock from '@/Components/Main/Dashboard/ContentBlock/Index.vue'
</script>

<template>
    <div class="row-span-2 grid grid-rows-2 gap-8">
        <ContentBlock v-for="(item, index) in projects.slice(0, 2)" :key="index" class="transition-all hover:ring-2 hover:ring-white cursor-pointer">
            <div class="flex items-center gap-8">
                <div class="w-20 h-20 bg-white rounded-2xl flex items-center justify-center">
                    <Image class="w-10 h-10" />
                </div>
                <div class="space-y-2">
                    <h3 class="text-lg font-semibold text-[#eaeaea]">{{ item.title }}</h3>
                    <p class="text-[#eaeaea]/60">{{ item.description }}</p>
                </div>
            </div>
            <div class="w-full flex justify-between">
                <div class="text-center py-1 px-4 font-semibold rounded-md bg-[#eaeaea]">Status</div>
                <div class="text-center pt-1 px-4 font-semibold rounded-md text-[#eaeaea] border-2 border-[#eaeaea]">
                    Priority</div>
            </div>
            <div class="w-full space-y-4">
                <h2 class="text-lg text-[#eaeaea] font-semibold">Tasks Completed: <span>25/60</span></h2>
                <div class="w-full bg-[#212429] rounded-full h-2.5 dark:bg-[#212429]">
                    <div class="bg-[#eaeaea] h-2.5 rounded-full" style="width: 45%"></div>
                </div>
            </div>
            <div class="w-full flex gap-4">
                <div v-for="(tag, index) in item.tags" :key="index"
                    class="py-1 px-4 bg-[#eaeaea] rounded-md shadow-md shadow-black/40">
                    {{ tag.name }}
                </div>
            </div>
            <div class="w-full">
                <p class="text-[#eaeaea] font-semibold">Deadline: <span>{{ item.deadline }}</span></p>
            </div>
        </ContentBlock>
    </div>
</template>