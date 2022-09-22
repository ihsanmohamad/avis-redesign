<script lang="ts">
	import { Container, Group, Button, createStyles } from '@svelteuidev/core';

	const useStyles = createStyles(() => ({
		root: {
			py: '$20',
			// borderRadius: '$lg',
            background: `url('Lines.svg')`,
            backgroundRepeat: 'no-repeat',
            backgroundSize: 'contain',
            backgroundPosition: 'center 100%',
			px: '$0',
			'@lg': {
				px: '$32'
			}
		},
		inner: {
			zIndex: '$5',
			display: 'flex',
			flexDirection: 'column',
			justifyContent: 'center',
            alignItems: 'center',
            mt: '$10',
			'@md': {
				flexDirection: 'row',
				mt: '$0'
			},
			'@xl': {
				mx: '$24'
			}
		},
		heroTitle: {
			color: '$black',
			fontSize: '40px',
			'@xl': {
				fontSize: '50px'
			}
		},
		heroCaption: {
			fontFamily: '$standard',
			fontStyle: 'normal',
			fontWeight: 400,
			fontSize: '20px',
			lineHeight: '150%',
			color: '#6A6D9E'
		},
		image: {
            height: '290px',
			'@md': {
				display: 'block',
				height: '290px'
			},
			'@lg': {
				height: '490px'
			},
			contain: 'content'
		},
		button: {
			background: '#4EA4F4',
			borderRadius: '20px',
			py: '$10',
			px: '$12',
			fontWeight: 500,
			'@md': {
				display: 'flex'
			}
		}
	}));

	$: ({ classes } = useStyles());
</script>

<div class={classes.root}>
	<Container fluid class={classes.inner}>
		<Group direction="column" align="baseline">
			<h1 class={classes.heroTitle}>Access Exclusive Privileges</h1>
			<p class={classes.heroCaption}>
				Treat yourself to 25% off published rates with Avis Malaysia Touch &#145;n Go Card and
				exclusive deals from our partners.
			</p>
			<Button class={classes.button}
				>More Partnership <svelte:fragment slot="rightIcon"
					><svg
						xmlns="http://www.w3.org/2000/svg"
						width="24"
						height="24"
						viewBox="0 0 24 24"
						fill="none"
						stroke="currentColor"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"><polyline points="9 18 15 12 9 6" /></svg
					></svelte:fragment
				></Button
			>
		</Group>
		<img class={classes.image} src="tng.png" alt="nice looking mobile app" />
	</Container>
</div>
