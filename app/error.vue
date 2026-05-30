<script setup lang="ts">
import type { NuxtError } from '#app'

const props = defineProps<{
    error: NuxtError
}>()

</script>


<template>
	<NuxtRouteAnnouncer />
    <UApp>
        <NuxtLayout>
			
            <UError :error="props.error" />

		</NuxtLayout>
    </UApp>
</template>
