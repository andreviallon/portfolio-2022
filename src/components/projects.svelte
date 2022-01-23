<script lang="ts">
	import ProjectCard from '../components/project-card.svelte';
	import type { Project } from 'src/model/project';

	const projects: Project[] = [
		{
			image: '../static/you-note.png',
			title: 'you note',
			description:
				'Note taking app for youtube videos. Past a video link and start taking notes as you watch it.',
			frontendStack: ['Angular', 'Tailwind'],
			backendStack: ['NestJS', 'Passport', 'Postgres'],
			websiteLink: 'https://you-note.vercel.app/',
			githubLink: 'https://github.com/andreviallon/you-note-frontend'
		},
		{
			image: '../static/invoice.png',
			title: 'invoice app',
			description: 'Full stack CRUD application to manage and create detailed invoices.',
			frontendStack: ['React', 'Next.js', 'Formik', 'Storybook'],
			backendStack: ['Node', 'MongoDB'],
			websiteLink: 'https://invoice-app-iota.vercel.app',
			githubLink: 'https://github.com/andreviallon/invoice-app'
		},
		{
			image: '../static/ip-tracker.png',
			title: 'ip address tracker',
			description:
				'Search for an IP address and get information about it, such as its location timezone and ISP.',
			frontendStack: ['Angular', 'NGXS', 'Leaflet'],
			websiteLink: 'https://ip-address-tracker-orcin.vercel.app/',
			githubLink: 'https://github.com/andreviallon/ip-address-tracker'
		},
		{
			image: '../static/calculator.png',
			title: 'calculator',
			description:
				'Your traditional calculator app... but with neat features, such as support for keyboard shortcuts and calculation chaining.',
			frontendStack: ['React', 'Next.js'],
			websiteLink: 'https://calculator-nine-sepia.vercel.app/',
			githubLink: 'https://github.com/andreviallon/calculator'
		}
	];
</script>

<div>
	<h2 class="font-bold text-3xl mb-12">projects</h2>
	<div class="grid grid-cols-1 lg:grid-cols-2	xl:grid-cols-3 gap-6">
		{#each projects as project}
			<ProjectCard {project} />
		{/each}
	</div>
</div>
