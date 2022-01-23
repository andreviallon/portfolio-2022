<script>
	import avatar from '../../static/avatar.png';
</script>

<div class="flex items-center justify-center w-full">
	<div class="avatar flex items-center justify-center">
		<div class="flex w-72 h-72 object-cover">
			<img
				src={avatar}
				class="w-72 h-72 object-cover z-20 absolute mt-4 ml-4 transition-all ease-in-out duration-300"
				alt="Avatar"
			/>
		</div>
		<div
			class="flex w-72 h-72 bg-gradient-to-r from-indigo-500 to-indigo-600 z-10 absolute mt-24 ml-24 avatar-background transition-all ease-in-out duration-300 shadow-lg shadow-indigo-300"
		/>
	</div>
</div>

<style lang="scss">
	img,
	.avatar-background {
		border-radius: 3rem;
	}
	.avatar:hover {
		img {
			margin-top: 0;
			margin-left: 0;
		}

		.avatar-background {
			margin-top: 8rem;
			margin-left: 8rem;
		}
	}
</style>
