<script lang="ts">
	import { Container, Group, createStyles } from '@svelteuidev/core';

	const useStyles = createStyles(() => ({
		root: {
			mt: '$40',
			// borderRadius: '$lg',
			zIndex: '$2',
			position: 'relative',
			px: '$0',
			background: 'linear-gradient(171.73deg, #D92C4E -1.67%, #82001A 98.89%);',
			'@lg': {
				px: '$32'
			}
		},
		inner: {
			zIndex: '$5',
			display: 'flex',
			flexDirection: 'column',
			justifyContent: 'stretch',
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
			color: '$white',
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
			color: '$white'
		},
		heroImage: {
            mt: '-90px',
			display: 'none',
			'@md': {
				display: 'block',
                height: '680px',
			},
			'@lg': {
                height: '680px',
			},
			contain: 'content'
		},
        actionImage: {
            cursor: 'pointer'
        },
		bookingBox: {
			zIndex: 10,
			my: '$12',
			padding: '$12',
			borderRadius: '20px',
			boxShadow: '0px 25px 50px rgba(0, 0, 0, 0.25)',
			border: '$black'
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
		<img class={classes.heroImage} src="mobile-app.png" alt="nice looking mobile app" />
		<Group direction="column" align="flex-start" override={{ my: '$24' }}>
			<h1 class={classes.heroTitle}>Convenience At Your Fingertips</h1>
			<p class={classes.heroCaption}>
				The Avis mobile app helps you find the right vehicle, make a booking, select the 'extras'
				you need, & track your loyalty rewards. Be in control of your bookings. Download the Avis
				mobile app today!
			</p>
			<div>
				<img class={classes.actionImage} src="android.png" alt="android play store link" />
				<img class={classes.actionImage} src="apple.png" alt="apple app store link" />
			</div>
		</Group>
	</Container>
</div>
