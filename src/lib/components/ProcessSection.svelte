<script lang="ts">
	import { Container, Group, Paper, Grid, Button, createStyles } from '@svelteuidev/core';

	const useStyles = createStyles(() => ({
		root: {
            py: '$24',
            position: 'relative',
			// borderRadius: '$lg',
			px: '$0',
			'@lg': {
				px: '$32'
			},
            '@md': {
                background: `url("map.svg")`,
                backgroundRepeat: 'no-repeat',
                backgroundSize: 'auto',
                backgroundPosition: 'center center'
            }
		},
		inner: {
			'@xl': {
				mx: '$24'
			}
		},
		title: {
			fontSize: '40px',
			'@xl': {
				fontSize: '50px'
			}
		},
		caption: {
			fontFamily: '$standard',
			fontStyle: 'normal',
			fontWeight: 400,
			fontSize: '20px',
			lineHeight: '150%',
			color: '#6A6D9E'
		},
        center: {
			my: '$12',
			alignItems: 'center',
			display: 'flex',
			flexDirection: 'column',
			justifyContent: 'center'
		},
		item: {
			height: '285px',
			alignItems: 'center',
			display: 'flex',
			flexDirection: 'column',
			justifyContent: 'space-evenly'
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
		<Group direction="column" align="flex-start">
			<h1 class={classes.title}>Fast & Convenient Experience</h1>
			<p class={classes.caption}>Hassle free and convenient! Speed up your booking with our service. We handle everything and you are ready to go. </p>
		</Group>
		<Grid justify="space-around" align="stretch" spacing="xs">
			<Grid.Col md={6} lg={4} xl={3}>
					<div class={classes.item}>
						<img src="Book.png" alt="booking process" />
                        <h4>Step 1</h4>
                        <p>Book your desired car with easy payment.</p>
					</div>
			</Grid.Col>
			<Grid.Col md={6} lg={4} xl={3}>
					<div class={classes.item}>
						<img src="Retrieve.png" alt="retrieve process" />
                            <h4>Step 2</h4>
                            <p>Meet up with our agent and retrieve the car.</p>
					</div>
			</Grid.Col>
			<Grid.Col md={6} lg={4} xl={3}>
					<div class={classes.item}>
						<img src="Drive.png" alt="drive process" />
                        <h4>Step 3</h4>
                        <p>Drive away!</p>
					</div>
			</Grid.Col>
			<Grid.Col md={6} lg={4} xl={3}>
					<div class={classes.item}>
						<img src="Return.png" alt="return process" />
                        <h4>Step 4</h4>
                        <p>Meet up with our agent and return the car.</p>
					</div>
			</Grid.Col>
		</Grid>
	</Container>
</div>
