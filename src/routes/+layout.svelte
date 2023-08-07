<script>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-hamlindigo.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import { text } from 'svelte/internal';
</script>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<a href="/">
					<strong class="text-xl uppercase">Prime Product Partners</strong>
				</a>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<a
					class="btn btn-sm variant-ghost-surface"
					href="/contact"
					rel="noreferrer"
				>
					Contact Us
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="/services"
					rel="noreferrer"
				>
					Our Services
				</a>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
	<!--Footer-->
	<svelte:fragment slot="pageFooter">
		<div class="flex flex-col items-center">
			<strong class="text-xl uppercase">Prime Product Partners</strong>
			<p class="text-l">info@primeproductpartners.com</p>
		</div>
	</svelte:fragment>
</AppShell>
