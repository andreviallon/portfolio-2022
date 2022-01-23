<script>
	import Header from '../components/header.svelte';
	import Hero from '../components/hero.svelte';
	import Avatar from '../components/avatar.svelte';
	import Projects from '../components/projects.svelte';
</script>

<div class="h-full">
	<Header />
	<div class="container mx-auto px-8 h-full">
		<div class="flex h-full">
			<div class="flex w-full xl:w-1/2">
				<Hero />
			</div>
			<div class="hidden xl:flex xl:w-1/2">
				<Avatar image={avatar} />
			</div>
		</div>
		<Projects />
	</div>
</div>
