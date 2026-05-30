<script setup lang="ts">

const route = useRoute();
const domain = computed(() => route.query.domain as string | undefined || route.params.domain as string | undefined);

useSeoMeta({
    title: "Domain Suspended | LeiCraft_MC Hosting",
    description: () => domain.value 
        ? "Die Domain " + domain.value + " wurde vorübergehend gesperrt." 
        : "Die Domain wurde vorübergehend gesperrt.",
});


</script>

<template>
    
    <div class="text-center">
        <h1 class="text-4xl font-bold mb-4">Domain Suspended</h1>

        <ClientOnly>
            <p v-if="domain" class="text-lg mb-2">
                Die Domain <strong>{{ domain }}</strong> wurde vorübergehend gesperrt.
            </p>

            <p v-else class="text-lg mb-2">Die Domain wurde vorübergehend gesperrt.</p>
            
            <template #fallback>
                <p class="text-lg mb-2">Die Domain wurde vorübergehend gesperrt.</p>
            </template>
        </ClientOnly>

        <p class="text-gray-600">
            Wenn Sie der Eigentümer dieser Domain sind, wenden Sie sich bitte an den Support unter <a href="mailto:support@leicraftmc.de" class="text-blue-500 underline">support@leicraft_mc.de</a>, um weitere Informationen zu erhalten.
        </p>
    </div>

</template>
