<script setup lang="ts">

useSeoMeta({
    title: "Redirecting... | LeiCraft_MC Hosting",
    description: "Sie werden weitergeleitet...",
});

await navigateTo("https://hosting.leicraftmc.de", { external: true });

</script>

<template>
    <div class="text-center">
        <h1 class="text-4xl font-bold mb-4">Redirecting...</h1>
        <p class="text-lg text-gray-600">Sie werden weitergeleitet...</p>
    </div>
</template>