<script setup lang="ts">
import MainLayout from '@/Layouts/MainLayout.vue';
import Search from '@/Components/Main/SearchInput/Index.vue'
import ProjectList from '@/Components/Main/Dashboard/ProjectList/Index.vue'
import TaskList from '@/Components/Main/Dashboard/TaskList/Index.vue'
import { Head } from '@inertiajs/vue3';

</script>

<template>

    <Head title="Dashboard" />

    <MainLayout>
        <Search class="mb-8" />
        <div class="w-full h-[90%] grid grid-cols-3 grid-rows-2 gap-8">
            <ProjectList />

            <div class="row-span-2 grid grid-rows-2 transition-all gap-8">
                <TaskList />
            </div>
        </div>
    </MainLayout>
</template>