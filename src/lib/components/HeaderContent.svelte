<script lang="ts">
	import { Container, Group, Button, Burger, createStyles } from '@svelteuidev/core';

	type items = {
		link: string;
		label: string;
	};

	const items: items[] = [
        { link: '/', label: 'Home' },
        { link: '/about', label: 'About Us' },
        { link: '/blog', label: 'Blog' },
        { link: '/booking', label: 'Your Booking' },
    ];

	const useStyles = createStyles((theme) => ({
		root: {
			marginTop: '$12',
			marginBottom: '$12'
		},
		inner: {
			display: 'flex',
			justifyContent: 'space-between',
			alignItems: 'center'
		},
		links: {
			display: 'none',
			'@md': {
				display: 'flex'
			}
		},
		link: {
			display: 'flex',
			lineHeight: 1,
			padding: '8px 12px',
			borderRadius: theme.radii.sm,
			textDecoration: 'none',
			color: '#1C1C1C',
			fontSize: '17px',
			fontWeight: 500,
			'&:hover': {
				backgroundColor: '#AF1433',
				borderRadius: '20px',
				color: '$white'
			},
			mx: '$9'
		},
		button: {
			background: '#4EA4F4',
			borderRadius: '20px',
			py: '$10',
			px: '$14',
			fontWeight: 500,
			display: 'none',
			'@md': {
				display: 'flex'
			}
		}
	}));

	$: ({ classes } = useStyles());
</script>

<div class={classes.root}>
	<Container class={classes.inner} fluid>
		<img src="logo.svg" alt="avis logo" href="/" />
		<Group spacing="xl" position="apart" class={classes.links}>
            {#each items as item }
    			<a class={classes.link} href={item.link}>{item.label}</a>
            {/each}
		</Group>
		<Button class={classes.button}>Sign Up</Button>
	</Container>
</div>
