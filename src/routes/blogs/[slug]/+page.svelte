<script lang="ts">
	import { marked } from 'marked';
	export let data;
	const post = data.post;

	const formattedContent = marked.parse(post.content);
</script>

<a href="/blogs" class="text-5xl pl-2 hover:text-blue-800 font-bold transition">&lt;---</a>
<article class="max-w-[1200px] mx-auto p-8 text-white rounded-xl shadow-xl mb-12 bg-[#141414]">
	<div class="border-b border-white/50">
		<!-- Post Title -->
		<div class="flex flex-row justify-between">
			<h1 class="text-3xl/6 md:text-7xl tracking-wider font-extrabold text-gradient mb-4 text-left">
				{post.title}
			</h1>
		</div>

		<!-- Post Date -->
		<p class="text-xl/6 md:text-3xl tracking-wide text-gray-400 text-right mb-6">{post.date}</p>
	</div>

	<!-- Excerpt -->
	<div
		class="prose prose-invert prose-a:text-blue-400 hover:prose-a:text-blue-600 prose-a:font-semibold prose-a:no-underline hover:prose-a:underline transition-colors duration-200 max-w-none text-xl/8 md:text-3xl mb-6 leading-relaxed tracking-tight"
	>
		{@html formattedContent}
	</div>
	<p class="text-xl/8 md:text-3xl text-gray-300 mt-6 tracking-wide text-right">- Hppingle</p>
</article>
