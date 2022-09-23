<script lang="ts">
	import { Container, Group, Button, createStyles } from '@svelteuidev/core';

	const useStyles = createStyles(() => ({
		root: {
            position: 'relative',
            mt: '$20',
            background: 'linear-gradient(180deg, #C2052A 0%, #570011 100%)',
			// borderRadius: '$lg',
			px: '$0',
			'@lg': {
                mt: '$20',
				px: '$32'
			},
		},
		inner: {
			display: 'flex',
			flexDirection: 'column-reverse',
			justifyContent: 'center',
			alignItems: 'center',
			mt: '$10',
			'@md': {
				display: 'flex',
				flexDirection: 'row',
				mt: '$0'
			},
			'@xl': {
				display: 'flex',
				flexDirection: 'row',
				mx: '$24'
			}
		},
		text: {
			fontFamily: '$standard',
			fontStyle: 'normal',
			fontWeight: 400,
			fontSize: '20px',
			lineHeight: '150%',
			color: 'white'
		},
		image: {
			width: '100%',
			'@md': {
				display: 'block',
				height: '290px'
			},
			'@lg': {
				height: '590px'
			},
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
			<p class={classes.text}>
				Need a vehicle for the long term but do not wish to buy one? Avis Car leasing is for you!
				You get to drive your car of choice with Avis taking care of all your vehicle maintenance
				and servicing needs.
			</p>
		</Group>
		<div>
			<p class={classes.text}>
				Need a vehicle for the long term but do not wish to buy one? Avis Car leasing is for you!
				You get to drive your car of choice with Avis taking care of all your vehicle maintenance
				and servicing needs.
			</p>
		</div>
	</Container>
</div>
