<script>
	export let data;
</script>

<!-- NAVBAR -->
<div class="flex w-full flex-row items-center border-b border-gray-700">
	<div
		class="max-w-[1200px] w-full flex flex-row items-center justify-between align-middle mx-auto px-2"
	>
		<p class="text-5xl font-extrabold uppercase font-vt323">Hppingle</p>
		<div class="flex flex-row space-x-4 text-3xl">
			<a href="/" class="uppercase hover:underline">Home</a>
			<a href="/" class="uppercase hover:underline">About</a>
		</div>
	</div>
</div>
<div class="mx-auto flex w-full max-w-[900px] flex-col p-4 items-center py-2">
	<!-- HEADER -->
	<h1 class="text-6xl uppercase tracking-wider py-2">Latest Posts</h1>

	<!-- POSTS -->
	<div class="flex flex-col py-2 gap-y-2 w-full items-center font-vt323">
		{#each data.posts as post}
			<div
				class="max-w-3xl w-full rounded-none border border-white/50 p-4 shadow-none hover:shadow-md transition flex flex-col"
			>
				<!-- Header -->
				<div class="flex flex-col space-y-4">
					<p class="text-2xl text-white/50">{post.date}</p>
					<h3 class="text-5xl text-whit font-extrabold tracking-wider">{post.title}</h3>
				</div>

				<!-- Content -->
				<div class="pt-4 text-white">
					<p class="mb-4 text-4xl">{post.topic}</p>
				</div>

				<!-- Footer -->
				<div class="flex items-center pt-4">
					<a
						href={`/blogs/${post.slug}`}
						class="text-2xl text-white underline hover:text-blue-600 transition"
					>
						Read more →
					</a>
				</div>
			</div>
		{/each}
	</div>
</div>
