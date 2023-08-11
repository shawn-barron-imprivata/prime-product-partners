<script>
	import '@skeletonlabs/skeleton/themes/theme-hamlindigo.css';
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import { text } from 'svelte/internal';
</script>

<AppShell>
	<svelte:fragment slot="header">
		<AppBar class="text-center">
			<svelte:fragment slot="lead">
				<a href="/">
					<img src="/images/ppp_logo.png" alt="company logo">
				</a>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<a class="btn btn-md variant-ghost-secondary" href="/contact" rel="noreferrer">
					Contact Us
				</a>
				<a class="btn btn-md variant-ghost-secondary" href="/services" rel="noreferrer">
					Our Services
				</a>
			</svelte:fragment>
			<div class="app-bar-content">
				<div class="center-container">
					<a href="/">
					<strong class="company-name text-4xl uppercase text-secondary-400">Prime Product Partners</strong>
					</a>
				</div>
			</div>
		</AppBar>
	</svelte:fragment>

	<slot />

	<svelte:fragment slot="pageFooter">
		<div class="flex flex-col items-center bg-gradient-to-br variant-gradient-surface-secondary">
			<strong class="text-xl uppercase">Prime Product Partners</strong>
			<p class="text-l">info@primeproductpartners.com</p>
		</div>
	</svelte:fragment>
</AppShell>

<style>
	img {
		max-width: 80px;
		max-height: 60px;
	}

	.app-bar-content {
		display: flex;
		justify-content: space-between;
		align-items: center;
		width: 100%;
	}

	.center-container {
		position: absolute;
		left: 50%;
		transform: translateX(-50%);
	}
</style>
