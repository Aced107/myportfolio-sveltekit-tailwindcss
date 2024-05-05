<script>
	// Declaring a prop named "step" to receive data from the parent component
	export let step;
</script>

<!-- Link to the project -->
<a
	href={step.href}
	target="_blank"
	class="group flex cursor-pointer flex-col gap-4 rounded-lg border border-solid border-violet-700 p-4 text-center duration-200 hover:border-violet-400 sm:p-6 md:p-8"
>
	<!-- Icon container -->
	<div
		class="mx-auto -mt-10 grid place-items-center bg-slate-950 px-4 text-5xl duration-200 sm:-mt-12 md:-mt-14 md:text-6xl lg:-mt-16"
	>
		<!-- Project icon rendered based on step.icon -->
		<i class={step.icon} />
	</div>
	<!-- Project name -->
	<h3 class="text-xl font-medium sm:text-2xl md:text-3xl">{step.name}</h3>
	<!-- Custom content provided by the parent component -->
	<slot />
	<!-- GitHub link -->
	<div class="flex flex-1 items-center justify-between gap-4">
		<!-- Link to the GitHub repository -->
		<a
			target="_blank"
			href={step.ghref}
			class="relative ml-auto cursor-pointer overflow-hidden duration-200 after:absolute after:right-full after:top-0 after:z-[-1] after:h-0 after:h-full after:w-full after:bg-white after:duration-200 hover:text-slate-950 hover:after:translate-x-full"
		>
			<!-- GitHub repo text -->
			<p class="z-4">GitHub Repo &rarr;</p>
		</a>
	</div>
</a>
