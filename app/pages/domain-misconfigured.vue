<script setup lang="ts">

const route = useRoute();
const domain = computed(() => route.query.domain as string | undefined || route.params.domain as string | undefined);

useSeoMeta({
    title: "Domain Misconfigured | LeiCraft_MC Hosting",
    description: () => domain.value 
        ? "Die Domain " + domain.value + " ist falsch konfiguriert." 
        : "Die Domain ist falsch konfiguriert.",
});

</script>

<template>
    
    <div class="text-center">
        <h1 class="text-4xl font-bold mb-4">Domain Misconfigured</h1>

        <ClientOnly>
            <p v-if="domain" class="text-lg mb-2">
                Die Domain <strong>{{ domain }}</strong> ist falsch konfiguriert.
            </p>

            <p v-else class="text-lg mb-2">Die Domain ist falsch konfiguriert.</p>

            <template #fallback>
                <p class="text-lg mb-2">Die Domain ist falsch konfiguriert.</p>
            </template>
        </ClientOnly>

        <p class="text-gray-600">
            Möglicherweise ist die Domain nicht korrekt auf unseren Servern eingerichtet.
            Bitte überprüfen Sie die DNS-Einstellungen Ihrer Domain und stellen Sie sicher, dass sie auf die richtigen Server zeigt.
            Bitte überprüfen Sie auch, ob die Domain auf unseren Servern korrekt registriert ist.
        </p>
    </div>

</template>
