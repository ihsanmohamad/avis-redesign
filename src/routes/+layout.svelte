<script lang="ts">
	import {
		SvelteUIProvider,
		Header,
		Container,
	} from '@svelteuidev/core';
	import HeaderContent from '$lib/components/HeaderContent.svelte';
</script>

<SvelteUIProvider withNormalizeCSS withGlobalStyles ssr>
		<!-- <Header height=60 override={{border: 'none' }} > -->
		<Header height=60 override={{ px: '$0', py: '$0', border: 'none','@lg': {px: '$32', py: '$6'} }} >
			<HeaderContent />
		</Header>
		<!-- <Container fluid override={{padding: 0}}> -->
		<!-- <Container fluid override={{ mt: '$0',S padding: 0, '@md': { padding: '$32' } }}> -->
			<slot />
		<!-- </Container> -->
</SvelteUIProvider>