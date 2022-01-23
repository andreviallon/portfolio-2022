<script>
	import Header from '../components/header.svelte';
	import Hero from '../components/hero.svelte';
	import Avatar from '../components/avatar.svelte';
	import Projects from '../components/projects.svelte';
	import About from '../components/about.svelte';
	import avatar from '../../static/avatar.png';

	const year = new Date().getFullYear();
</script>

<div class="h-full">
	<Header />
	<div class="container mx-auto px-8 h-full">
		<div class="flex hero-container">
			<div class="flex w-full xl:w-1/2">
				<Hero />
			</div>
			<div class="hidden xl:flex xl:w-1/2">
				<Avatar image={avatar} />
			</div>
		</div>
		<Projects />
		<div class="mt-32">
			<About />
		</div>
		<p class="mt-48 mb-24 flex justify-center w-full">
			©{year} Andre viallon, all rights reserved.
		</p>
	</div>
</div>

<style lang="scss">
	.hero-container {
		height: 100vh;
	}
</style>
