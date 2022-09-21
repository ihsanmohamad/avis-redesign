<script>
	import AppSection from 'lib/components/AppSection.svelte';
import CategorySection from 'lib/components/CategorySection.svelte';
	import HeroSection from 'lib/components/HeroSection.svelte';
	import ProcessSection from 'lib/components/ProcessSection.svelte';
</script>

<svelte:head>
	<title>Avis Car Rental</title>
</svelte:head>

<!-- <div style="display: flex;
align-items: center;
flex-direction:column;
justify-content: center;">
    <h1>Welcome to SvelteKit</h1>
    <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
</div> -->
<div style="background: #F2F6FF;">
    <HeroSection />
    <CategorySection />
    <ProcessSection />
    <AppSection />
</div>
