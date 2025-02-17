<script setup lang="ts">
import { Link } from '@inertiajs/vue3';
import { Album, Calendar, CalendarRange, CheckSquare, Clock, Dribbble, LayoutDashboard, LayoutTemplate, Mail, MessageSquare, Settings, TerminalSquare, Timer } from 'lucide-vue-next';
</script>

<template>
    <div class="w-full min-h-screen bg-[#17191C] p-2">
        <div class="w-full h-main bg-[#212429] rounded-3xl flex">
            <div class="h-full w-[15%] bg-[#2b2e33] rounded-l-3xl shadow-[4px_0_15px_#000000] !shadow-black/40 py-8">
                <div class="w-full px-4 h-full mx-auto flex flex-col gap-12">
                    <Dribbble class="text-[#eaeaea] h-16 w-16 mx-auto" />
                    <ul class="flex flex-col gap-4">
                        <li>
                            <Link :href="'#!'"
                                class="flex items-center gap-4 py-2 px-4 transition-all hover:gap-6 hover:bg-gradient-to-r hover:from-black/20 hover:to-transparent">
                            <LayoutDashboard class="w-8 h-8 text-[#eaeaea]" />
                            <span class="text-lg font-semibold text-[#eaeaea]">Dashboard</span>
                            </Link>
                        </li>
                        <li>
                            <Link :href="'#!'"
                                class="flex items-center gap-4 py-2 px-4 transition-all hover:gap-6 hover:bg-gradient-to-r hover:from-black/20 hover:to-transparent">
                            <TerminalSquare class="w-8 h-8 text-[#eaeaea]" />
                            <span class="text-lg font-semibold text-[#eaeaea]">Projects</span>
                            </Link>
                        </li>
                        <li>
                            <Link :href="'#!'"
                                class="flex items-center gap-4 py-2 px-4 transition-all hover:gap-6 hover:bg-gradient-to-r hover:from-black/20 hover:to-transparent">
                            <CheckSquare class="w-8 h-8 text-[#eaeaea]" />
                            <span class="text-lg font-semibold text-[#eaeaea]">Tasks</span>
                            </Link>
                        </li>
                        <li>
                            <Link :href="'#!'"
                                class="flex items-center gap-4 py-2 px-4 transition-all hover:gap-6 hover:bg-gradient-to-r hover:from-black/20 hover:to-transparent">
                            <CalendarRange class="w-8 h-8 text-[#eaeaea]" />
                            <span class="text-lg font-semibold text-[#eaeaea]">Calendar</span>
                            </Link>
                        </li>
                        <li>
                            <Link :href="'#!'"
                                class="flex items-center gap-4 py-2 px-4 transition-all hover:gap-6 hover:bg-gradient-to-r hover:from-black/20 hover:to-transparent">
                            <Clock class="w-8 h-8 text-[#eaeaea]" />
                            <span class="text-lg font-semibold text-[#eaeaea]">Time Manage</span>
                            </Link>
                        </li>
                        <li>
                            <Link :href="'#!'"
                                class="flex items-center gap-4 py-2 px-4 transition-all hover:gap-6 hover:bg-gradient-to-r hover:from-black/20 hover:to-transparent">
                            <Mail class="w-8 h-8 text-[#eaeaea]" />
                            <span class="text-lg font-semibold text-[#eaeaea]">Reports</span>
                            </Link>
                        </li>
                        <li>
                            <Link :href="'#!'"
                                class="flex items-center gap-4 py-2 px-4 transition-all hover:gap-6 hover:bg-gradient-to-r hover:from-black/20 hover:to-transparent">
                            <Settings class="w-8 h-8 text-[#eaeaea]" />
                            <span class="text-lg font-semibold text-[#eaeaea]">Settings</span>
                            </Link>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="w-[85%] p-8">
                <slot />
            </div>
        </div>
    </div>
</template>

<style scoped>
    .h-main {
        height: calc(100vh - 16px);
    }
</style>