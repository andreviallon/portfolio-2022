<script>
	let isMenuOpen = false;

	const toggleMenu = () => {
		isMenuOpen = !isMenuOpen;
	};
</script>

<header class="fixed top-0 left-0 right-0 z-50 bg-gray-100">
	<div class="flex py-8 px-10 justify-between items-center">
		<a class="text-xl bottom-bar-on-hover" href="/"> andré viallon </a>
		<div class="hidden sm:flex">
			<a href="/" class="bottom-bar-on-hover ml-10" on:click={toggleMenu}> projects </a>
			<a href="/" class="bottom-bar-on-hover ml-10" on:click={toggleMenu}> about </a>
			<a href="/" class="bottom-bar-on-hover ml-10" target="_blank" rel="noreferrer"> resume </a>
		</div>

		<div class="flex sm:hidden cursor-pointer">
			{#if isMenuOpen}
				<span on:click={toggleMenu}>close</span>
			{:else}
				<span on:click={toggleMenu}>menu</span>
			{/if}
		</div>
	</div>
</header>
{#if isMenuOpen}
	<div
		class="fixed top-0 right-0 left-0 bottom-0 bg-gray-100 sm:hidden flex justify-center items-center z-10"
	>
		<div class="flex flex-col items-center mt-12">
			<a class="text-2xl mb-10" href="/" on:click={toggleMenu}> projects </a>
			<a class="text-2xl mb-10" href="/" on:click={toggleMenu}> about </a>
			<a href={'resume.pdf'} target="_blank" rel="noreferrer" class="text-2xl mb-10"> resume </a>
		</div>
	</div>
{/if}

<style>
	a {
		@apply font-medium text-lg cursor-pointer;
	}

	span {
		@apply font-medium;
	}
</style>
