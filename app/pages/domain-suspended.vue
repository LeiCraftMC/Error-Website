<script setup lang="ts">

const domain = useRoute().params.domain

if (typeof domain === "string") {

    useSeoMeta({
        title: "Domain Suspended | LeiCraft_MC Hosting",
        description: "Die Domain " + domain + " wurde vorübergehend gesperrt.",
    });

} else {

    useSeoMeta({
        title: "Domain Suspended | LeiCraft_MC Hosting",
        description: "Die Domain wurde vorübergehend gesperrt.",
    });

}

</script>

<template>
    
    <div class="text-center">
        <h1 class="text-4xl font-bold mb-4">Domain Suspended</h1>

        <p v-if="typeof domain === 'string'" class="text-lg mb-2">
            Die Domain <strong>{{ domain }}</strong> wurde vorübergehend gesperrt.
        </p>

        <p v-else class="text-lg mb-2">Die Domain wurde vorübergehend gesperrt.</p>

        <p class="text-gray-600">
            Wenn Sie der Eigentümer dieser Domain sind, wenden Sie sich bitte an den Support unter <a href="mailto:support@leicraftmc.de" class="text-blue-500 underline">support@leicraft_mc.de</a>, um weitere Informationen zu erhalten.
        </p>
    </div>

</template>
