<script lang="ts">
	import StackList from './stack-list.svelte';
	import type { Project } from 'src/model/project';
	import { faKeyboard } from '@fortawesome/free-regular-svg-icons';
	import { faDatabase } from '@fortawesome/free-solid-svg-icons';

	export let project: Project;
	let isHovering = false;

	const enter = () => {
		isHovering = true;
	};

	const leave = () => {
		isHovering = false;
	};
</script>

<div
	class="project-card flex flex-col justify-between p-4 bg-white rounded-2xl w-full shadow-lg hover:-translate-y-2 h-full"
	on:mouseenter={enter}
	on:mouseleave={leave}
>
	<div>
		<img src={project.image} class="rounded-2xl w-full h-72 object-cover" alt="Avatar" />
		<h2 class="text-2xl font-bold pt-4 hover:text-white">{project.title}</h2>
		<p class="text-base pt-4 text-slate-500 hover:text-slate-200">{project.description}</p>

		{#if !!project.frontendStack?.length}
			<div class="flex items-center pt-2 text-slate-500 hover:text-slate-200">
				<StackList
					{isHovering}
					text="Frontend"
					icon={faKeyboard}
					stackList={project.frontendStack}
				/>
			</div>
		{/if}

		{#if !!project.backendStack?.length}
			<div class="flex items-center pt-2 text-slate-500 hover:text-slate-200">
				<StackList {isHovering} text="Backend" icon={faDatabase} stackList={project.backendStack} />
			</div>
		{/if}
	</div>
	<div>
		<div class="flex gap-4 mt-6">
			<a
				class="text-center py-2 px-4 rounded-md text-neutral-900 font-medium w-full border-solid border-indigo-400 border-2 hover:-translate-y-1"
				target="_blank"
				href={project.githubLink}
				rel="noopener noreferrer"
			>
				view code
			</a>

			<a
				class="text-center py-2 px-4 rounded-md text-white font-medium w-full bg-gradient-to-r from-indigo-400 to-indigo-600 hover:-translate-y-1"
				target="_blank"
				href={project.websiteLink}
				rel="noopener noreferrer"
			>
				live demo
			</a>
		</div>
	</div>
</div>

<style lang="scss">
	.project-card {
		@apply transition ease-in-out duration-300;

		&:hover {
			@apply bg-neutral-900;

			h2,
			p,
			a {
				@apply text-white;
			}
		}
	}
</style>
