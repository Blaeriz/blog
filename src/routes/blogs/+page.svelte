<script>
	export let data;
</script>

<!-- NAVBAR -->
<div class="flex w-full flex-row items-center border-b border-gray-700">
	<div
		class="max-w-[1200px] w-full flex flex-row items-center justify-between align-middle mx-auto px-2"
	>
		<a href="/" class="text-5xl font-extrabold uppercase font-vt323">Hppingle</a>
		<div class="flex flex-row space-x-4 text-3xl">
			<a href="/" class="uppercase text-blue-600 hover:underline">Blogs</a>
			<a href="/about" class="uppercase hover:underline">About</a>
		</div>
	</div>
</div>
<div class="mx-auto flex w-full max-w-[900px] flex-col p-4 items-center py-2">
	<!-- HEADER -->
	<h1 class="text-xl/8 md:text-5xl uppercase tracking-wider py-2">Latest Posts</h1>

	<!-- POSTS -->
	<div class="flex flex-col py-2 gap-y-2 w-full items-center font-vt323">
		{#each data.posts as post}
			<div
				class="max-w-3xl w-full rounded-none border border-white/50 p-4 shadow-none hover:shadow-md transition flex flex-col"
			>
				<!-- Header -->
				<div class="flex flex-col space-y-4">
					<div class="flex flex-row justify-between">
						<p class="text-lg md:text-2xl text-white/50">{post.date}</p>
						<p class="text-lg md:text-2xl text-white/50">
							Read Time: {post.word_count / 200}m
						</p>
					</div>
					<h3 class="text-2xl md:text-5xl text-whit font-extrabold tracking-wider">{post.title}</h3>
				</div>

				<!-- Content -->
				<div class="pt-4 text-white">
					<p class="mb-4 text-2xl md:text-4xl">{post.topic}</p>
				</div>

				<!-- Footer -->
				<div class="flex flex-row justify-between pt-4">
					<a
						href={`/blogs/${post.slug}`}
						class="text-lg md:text-2xl text-white underline hover:text-blue-600 transition"
					>
						Read more →
					</a>
					{#if post.tags && post.tags.length > 0}
						<p class="text-lg md:text-2xl text-white/50 mt-2 md:mt-0">
							{post.tags.join(', ')}
						</p>
					{/if}
				</div>
			</div>
		{/each}
	</div>
</div>
