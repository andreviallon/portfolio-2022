<script>
	import Button from '../components/button.svelte';
</script>

<div class="h-full flex flex-col justify-center">
	<div class="mb-6">
		<p class="text-3xl sm:text-5xl mb-2 sm:mb-4 font-medium">hi there!</p>
		<p class="text-3xl sm:text-5xl mb-2 sm:mb-4 font-medium">my name is andré,</p>
		<p class="text-3xl sm:text-5xl mb-2 sm:mb-4 font-medium">i’m a frontend engineer.</p>
	</div>
	<div class="leading-10">
		<span>
			Welcome to my portfolio. Here you can have a look at my personal work and learn more about me.
			You can also see more of my coding projects on{' '}
			<a
				class="hide-bottom-bar-on-hover"
				href="https://github.com/andreviallon"
				target="_blank"
				rel="noreferrer"
			>
				github
			</a>
			, connect with my on
			<a
				class="hide-bottom-bar-on-hover bold"
				href="https://www.linkedin.com/in/andre-viallon"
				target="_blank"
				rel="noreferrer"
			>
				linkedin
			</a>
			or simply send me an
			<a
				class="hide-bottom-bar-on-hover bold"
				href="mailto:viallon.andre@gmail.com"
				rel="noopener noreferrer"
			>
				email
			</a>
			.
		</span>
	</div>
	<div class="mt-8">
		<Button text="learn more" />
	</div>
</div>
