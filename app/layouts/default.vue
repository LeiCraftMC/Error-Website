<script setup lang="ts">
import LCMCIcon from "~/components/img/LCMCIcon.vue";


</script>

<template>

    <div class="app-layout main-bg-color">

        <UHeader>
            <template #left>
                <!-- Überschreibt den Standard Nuxt UI Text -->
                <div class="hidden"></div>
            </template>

            <template #default>
                <NuxtLink to="/" :class="`flex items-center gap-1.5`">
                    <LCMCIcon class="w-10 h-10" />
                    <span class="text-3xl font-extrabold">
                        LeiCraft_MC Hosting
                    </span>
                </NuxtLink>
            </template>

        </UHeader>

        <UMain class="py-8 main-content flex flex-col justify-center">
            <UContainer class="w-full">
                <div class="border-4 border-gray-300 p-6 rounded-lg">
                    <slot />
                </div>
            </UContainer>
        </UMain>

        <UFooter class="mt-8 bg-neutral-900">
            <div class="text-sm text-slate-500 text-center">
                &copy; {{ new Date().getFullYear() }} LeiCraft_MC. All rights reserved.
            </div>
        </UFooter>

    </div>

</template>

<style scoped>
.app-layout {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}

.main-content {
    flex: 1;
}
</style>