<script lang="ts">
	import { Container, Group, Paper, Grid, Button, createStyles } from '@svelteuidev/core';

	const useStyles = createStyles(() => ({
		root: {
			pt: '$16',
			// borderRadius: '$lg',
			px: '$0',
			'@lg': {
				px: '$32'
			},
			background: '#F2F6FF'
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
		categoryItem: {
			height: '285px',
			alignItems: 'center',
			display: 'flex',
			flexDirection: 'column',
			justifyContent: 'space-evenly'
		},
		categoryCard: {
			my: '$12',
			boxShadow: '0px 21.9319px 43.8639px rgba(0, 0, 0, 0.15)',
			zIndex: '$1',
			position: 'relative',
			borderRadius: '25px',
			'&::before': {
				zIndex: '-1',
				content: `''`,
				position: 'absolute',
				background: '#D1052D',
				top: '0',
				left: '0',
				width: '90px',
				height: '40px',
				borderTopLeftRadius: '25px',
				borderBottomLeftRadius: '0px',
				borderTopRightRadius: '0px',
				borderBottomRightRadius: '8px'
			}
		},
		badge: {
			position: 'absolute',
			zIndex: '$10',
			fontSize: '15px',
			fontWeight: '400',
			ml: '$2',
			mt: '-$2',
			color: '$white'
		},
		categoryButton: {
			borderRadius: '15px',
			borderColor: '#CAD6F1',
			borderWidth: '1.5px',
			color: '4EA4F4',
			py: '$10',
			px: '$18',
			fontWeight: 500,
			'@md': {
				display: 'flex'
			}
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
		},
		center: {
			my: '$12',
			alignItems: 'center',
			display: 'flex',
			flexDirection: 'column',
			justifyContent: 'center'
		}
	}));

	$: ({ classes } = useStyles());
</script>

<div class={classes.root}>
	<Container fluid class={classes.inner}>
		<Group direction="column" align="flex-start">
			<h1 class={classes.title}>Categories</h1>
			<p class={classes.caption}>Check out our most popular cars by categories</p>
		</Group>
		<Grid justify="space-around" align="stretch" spacing="xs">
			<Grid.Col md={6} lg={4} xl={3}>
				<Paper class={classes.categoryCard} withBorder>
					<span class={classes.badge}>Mini</span>
					<div class={classes.categoryItem}>
						<img src="Axia.png" alt="Kereta axia pehhh" />
						<Button class={classes.categoryButton} variant="outline">View</Button>
					</div>
				</Paper>
			</Grid.Col>
			<Grid.Col md={6} lg={4} xl={3}>
				<Paper class={classes.categoryCard} withBorder>
					<span class={classes.badge}>Sedan</span>
					<div class={classes.categoryItem}>
						<img src="Sedan.png" alt="Padu baq hang sedan" />
						<Button class={classes.categoryButton} variant="outline">View</Button>
					</div>
				</Paper>
			</Grid.Col>
			<Grid.Col md={6} lg={4} xl={3}>
				<Paper class={classes.categoryCard} withBorder>
					<span class={classes.badge}>MPV</span>
					<div class={classes.categoryItem}>
						<img src="MPV.png" alt="Mantul MPV" />
						<Button class={classes.categoryButton} variant="outline">View</Button>
					</div>
				</Paper>
			</Grid.Col>
		</Grid>
		<div class={classes.center}>
			<Button class={classes.button}
				>See More <svelte:fragment slot="rightIcon"
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
		</div>
	</Container>
</div>
