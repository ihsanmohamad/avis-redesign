<script lang="ts">
	import { Container, Group, Paper, SimpleGrid, Button, createStyles } from "@svelteuidev/core";

    const useStyles = createStyles(() => ({
        root: {
            mt: '$10',
            // borderRadius: '$lg',
            zIndex: '$2',
            position: 'relative',
            px: '$0',
            height: '600px',
            overflow: 'hidden',
            background: 'linear-gradient(180deg, #C90027 -2.78%, #B90C2E 75.97%, #97001E 97.06%)',
            '&::before': {
                content: `''`,
                position: 'absolute',
                background: 'white',
                transform: 'rotate(-5deg)',
                top: '-43%',
                left: '-30%',
                width: '5000px',
                height: '400px',
                zIndex: -1
            },
            '@lg': {
                px: '$32'
            },
        },
        inner: {
            zIndex: '$5',
			display: 'flex',
            flexDirection: 'column',
			justifyContent: 'space-between',
            mt: '$10',
            '@md': {
                flexDirection: 'row',
                mt: '$0',
            },
            '@xl': {
				mx: '$24'
			}
		},
        heroTitle: {
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
            color: '#6A6D9E',
        },
        heroImage: {
            display: 'none',
            width: '300px',
            '@md': {
                display: 'block',
                width: '700px'
            },
            '@lg': {
                width: '100%'
            },
            contain: 'content'
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

    $: ({classes} = useStyles())
</script>
<div class={classes.root}>
    <Container fluid class={classes.inner}>
        <Group direction="column" align="flex-start">
            <h1 class={classes.heroTitle}>What will you be driving today?</h1>
            <p class={classes.heroCaption}>Avis provides customers professional mobility services and solutions specializing in vehicle rental, leasing and fleet management.</p>
        </Group>
            <img class={classes.heroImage} src="X50.png" alt="nice looking car" />
    </Container>
    <Container override={{mt: '$28', '@md': {mt: '$0'}}}>
        <Paper class={classes.bookingBox} withBorder>
            <SimpleGrid cols={4} spacing="md" >
                <div>1</div>
                <div>2</div>
                <div>3</div>
                <Button class={classes.button}>Search Car</Button>
            </SimpleGrid>
          </Paper>
    </Container>
</div>