<script lang="ts">
	import ProjectCard from '../components/project-card.svelte';
	import type { Project } from 'src/model/project';
	import youNoteImg from '../../static/you-note.png';
	import invoiceImg from '../../static/invoice.png';
	import ipTrackerImg from '../../static/ip-tracker.png';
	import calculatorImg from '../../static/calculator.png';

	const projects: Project[] = [
		{
			image: youNoteImg,
			title: 'you note',
			description:
				'Note taking app for youtube videos. Past a video link and start taking notes as you watch it.',
			frontendStack: ['Angular', 'Tailwind'],
			backendStack: ['NestJS', 'Passport', 'Postgres'],
			websiteLink: 'https://you-note.vercel.app/',
			githubLink: 'https://github.com/andreviallon/you-note-frontend'
		},
		{
			image: invoiceImg,
			title: 'invoice app',
			description: 'Full stack CRUD application to manage and create detailed invoices.',
			frontendStack: ['React', 'Next.js', 'Formik', 'Storybook'],
			backendStack: ['Node', 'MongoDB'],
			websiteLink: 'https://invoice-app-iota.vercel.app',
			githubLink: 'https://github.com/andreviallon/invoice-app'
		},
		{
			image: ipTrackerImg,
			title: 'ip address tracker',
			description:
				'Search for an IP address and get information about it, such as its location timezone and ISP.',
			frontendStack: ['Angular', 'NGXS', 'Leaflet'],
			websiteLink: 'https://ip-address-tracker-orcin.vercel.app/',
			githubLink: 'https://github.com/andreviallon/ip-address-tracker'
		},
		{
			image: calculatorImg,
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
