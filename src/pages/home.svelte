<script lang="ts">
	import Header from '../components/header.svelte';
	import Hero from '../components/hero.svelte';
	import Avatar from '../components/avatar.svelte';
	import Projects from '../components/projects.svelte';
	import About from '../components/about.svelte';
	import avatar from '../../static/avatar_hero.jpg';
	import * as animateScroll from 'svelte-scrollto';
	import Notifications from 'svelte-notifications';

	function handleScrollTo(el): void {
		animateScroll.scrollTo({ element: `#${el.detail}`, offset: -100 });
	}

	const year = new Date().getFullYear();
</script>

<svelte:head>
	<title>Andre Viallon | Portfolio</title>
</svelte:head>
<Notifications>
	<div class="h-full" id="header">
		<Header on:navigateTo={(el) => handleScrollTo(el)} />
		<div class="container mx-auto px-8 h-full">
			<div class="flex hero-container">
				<div class="flex w-full xl:w-1/2">
					<Hero on:navigateTo={(el) => handleScrollTo(el)} />
				</div>
				<div class="hidden xl:flex xl:w-1/2">
					<Avatar image={avatar} />
				</div>
			</div>
			<div id="projects" />
			<Projects />
			<div class="mt-32">
				<div id="about" />
				<About />
			</div>
			<p class="mt-48 mb-24 flex justify-center w-full">
				©{year} Andre viallon, all rights reserved.
			</p>
		</div>
	</div>
</Notifications>

<style lang="scss">
	.hero-container {
		height: 100vh;
	}
</style>
