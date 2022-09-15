<script lang="ts">
	import { Container, createStyles } from "@svelteuidev/core";

    const useStyles = createStyles(() => ({
        root: {
            zIndex: '$2',
            position: 'relative',
            px: '$32',
            height: '500px',
            overflow: 'hidden',
            background: 'linear-gradient(180deg, #C90027 -2.78%, #B90C2E 75.97%, #97001E 97.06%)',
            '&::before': {
                content: `''`,
                position: 'absolute',
                background: 'white',
                transform: 'rotate(-5deg)',
                top: '-50%',
                left: '-30%',
                width: '5000px',
                height: '300px',
                zIndex: -1
            }
        },
        inner: {
            zIndex: '$5',
			display: 'flex',
			justifyContent: 'space-between',
			alignItems: 'center'
		},
	}));

    $: ({classes} = useStyles())
</script>
<div class={classes.root}>
    <Container fluid class={classes.inner}>
        <h1>Welcome to SvelteKit</h1>
        <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
    </Container>
</div>