<script setup lang="ts">

const domain = useRoute().params.domain

if (typeof domain === "string") {

    useSeoMeta({
        title: "Domain Misconfigured | LeiCraft_MC Hosting",
        description: "Die Domain " + domain + " ist falsch konfiguriert.",
    });

} else {

    useSeoMeta({
        title: "Domain Misconfigured | LeiCraft_MC Hosting",
        description: "Die Domain ist falsch konfiguriert.",
    });

}

</script>

<template>
    
    <div class="text-center">
        <h1 class="text-4xl font-bold mb-4">Domain Misconfigured</h1>

        <p v-if="typeof domain === 'string'" class="text-lg mb-2">
            Die Domain <strong>{{ domain }}</strong> ist falsch konfiguriert.
        </p>

        <p v-else class="text-lg mb-2">Die Domain ist falsch konfiguriert.</p>

        <p class="text-gray-600">
            Möglicherweise ist die Domain nicht korrekt auf unseren Servern eingerichtet.
            Bitte überprüfen Sie die DNS-Einstellungen Ihrer Domain und stellen Sie sicher, dass sie auf die richtigen Server zeigt.
            Bitte überprüfen Sie auch, ob die Domain auf unseren Servern korrekt registriert ist.
        </p>
    </div>

</template>
