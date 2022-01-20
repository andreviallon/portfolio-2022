<script>
	let isMenuOpen = false;

	const toggleMenu = () => {
		isMenuOpen = !isMenuOpen;
	};
</script>

<header class="fixed top-0 left-0 right-0 z-20">
	<div class="flex py-8 px-10 justify-between items-center">
		<a class="font-medium text-xl bottom-bar-on-hover cursor-pointer bottom-bar-on-hover" href="/">
			andré viallon
		</a>
		<div class="hidden sm:flex">
			<a
				class="font-medium text-lg bottom-bar-on-hover cursor-pointer"
				href="/"
				on:click={toggleMenu}
			>
				portfolio
			</a>
			<a
				class="font-medium text-lg ml-10 bottom-bar-on-hover cursor-pointer"
				href="/"
				on:click={toggleMenu}
			>
				about
			</a>
			<a
				href="/"
				target="_blank"
				rel="noreferrer"
				class="font-medium text-lg ml-10 bottom-bar-on-hover cursor-pointer"
			>
				resume
			</a>
		</div>

		<div class="flex sm:hidden cursor-pointer">
			{#if isMenuOpen}
				<span class="font-medium" on:click={toggleMenu}>close</span>
			{:else}
				<span class="font-medium" on:click={toggleMenu}>menu</span>
			{/if}
		</div>
	</div>

	{#if isMenuOpen}
		<div
			class="fixed top-0 right-0 left-0 bottom-0 bg-gray-200 sm:hidden flex justify-center items-center z-10"
		>
			<div class="flex flex-col items-center mt-12">
				<a class="font-medium text-2xl mb-10" href="/" on:click={toggleMenu}> portfolio </a>
				<a class="font-medium text-2xl mb-10" href="/" on:click={toggleMenu}> about </a>
				<a href={'resume.pdf'} target="_blank" rel="noreferrer" class="font-medium text-2xl mb-10">
					resume
				</a>
			</div>
		</div>
	{/if}
</header>
