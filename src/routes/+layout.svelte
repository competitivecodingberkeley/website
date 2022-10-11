<script>
	import Logo from '../logo.png';
</script>

<svelte:head>
	<title>Competitive Coding @ Berkeley</title>
</svelte:head>

<div class="section is-small">
	<div class="container">
		<div class="header">
			<img src={Logo} width="150" />
			<div class="header-content">
				<p class="paragraph">
					<a class="s-4" href="/"><b>Competitive Coding</b> @ Berkeley</a>
				</p>
				<p class="paragraph">
					<a href="/">about</a>
					<a href="#team">team</a>
					<a href="#contact">contact</a>
				</p>
			</div>
		</div>
	</div>
</div>
<slot />

<style>
	.header {
		display: flex;
		align-items: center;
	}

	.header-content {
		margin-left: 1em;
	}

	a {
		color: var(--blue);
		font-family: 'IBM Plex Mono';
	}

	a + a {
		margin-left: 1ch;
	}
</style>
