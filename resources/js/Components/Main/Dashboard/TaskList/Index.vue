<script setup lang="ts">
import ContentBlock from '@/Components/Main/Dashboard/ContentBlock/Index.vue'

const tasks = [
    {
        title: 'Example title'
    },
    {
        title: 'Example title'
    },
    {
        title: 'Example title'
    },
    {
        title: 'Example title'
    },
    {
        title: 'Example title'
    },
    {
        title: 'Example title'
    },
    {
        title: 'Example title'
    },
]
</script>

<template>
    <ContentBlock>
        <h2 class="text-xl font-semibold text-[#eaeaea]">My Tasks (<stan>{{ tasks?.length }}</stan>)</h2>
        <ul class="flex flex-col gap-2">
            <li v-for="(item, index) in tasks" :key="index">
                <div :class="index > 3 ? 'opacity-50' : ''"
                    class="flex items-center justify-between py-2 border-b border-[#212429] text-[#eaeaea]">
                    <div class="flex items-center gap-4" :class="index > 4 ? 'opacity-25' : ''">
                        <span class="w-4">
                            {{ index + 1 }}
                        </span>
                        <h3>{{ item.title }}</h3>
                    </div>
                    <input :disabled="index > 3" type="checkbox" class="rounded-full">
                </div>
            </li>
        </ul>
    </ContentBlock>
</template>