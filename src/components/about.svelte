<script>
	import Button from '../components/button.svelte';
	import Avatar from '../components/avatar.svelte';
	import avatar from '../../static/avatar2.jpg';
</script>

<div>
	<h2 class="font-bold text-3xl mb-12">about</h2>
	<div class="flex flex-col lg:flex-row items-start gap-6">
		<div class="text-gray-500 leading-7">
			<p class="pb-2">
				So, this is where I get to talk a bit about myself. My name is André. I’m a Frontend
				Engineer with a great passion for creating beautiful, modern and intuitive User Interfaces.
			</p>
			<p class="pb-2">
				I’ve always watned to push myself and learn more. That’s why I left France, my home country,
				to move to Denmark back in 2012 where I joined the International Baccalaureate in
				Sønderborg. I then went on with studying Web Development as well as UI desing at the
				International Business Academy in Kolding.
			</p>

			<p class="pb-2">
				In my spare time I enjoy, playing the guitar, reading books, wathcing movies, going on
				hikes, biking, doing yoga or coding side projects.
			</p>

			<p class="pb-2">
				I encourage you to checkout my resume to learn more about my past experience and my skills.
			</p>
			<div class="mt-4">
				<Button text="open resume" />
			</div>
		</div>
		<Avatar image={avatar} isRightAlign={true} />
	</div>
</div>
