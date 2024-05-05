<!-- 
    This is the Header component responsible for displaying the header of the web application.
    It includes the site name, navigation tabs, and a "Get in touch" button.
-->

<script>
	// Exporting a prop 'y' representing the vertical scroll position
	export let y;

	// Array of tabs with their names and corresponding links
	let tabs = [
		{ name: 'Projects', link: '#projects' },
		{ name: 'About me', link: '#about' }
	];
</script>

<!-- Header section -->
<header
	class={'sticky top-0 z-[10] flex items-center justify-between border-b border-solid px-6 duration-200 ' +
		// Conditionally applying styles based on scroll position
		(y > 0 ? ' border-violet-950 bg-slate-950 py-4' : ' border-transparent bg-transparent py-6')}
>
	<!-- Site name -->
	<h1 class="font-medium">
		<b class="poppins font-bold">Armaan</b> Mohammad
	</h1>

	<!-- Navigation tabs -->
	<div class="ml-auto hidden items-center gap-4 pr-4 sm:flex">
		{#each tabs as tab, index}
			<a class="duration-200 hover:text-violet-400" href={tab.link}>
				<p>{tab.name}</p>
			</a>
		{/each}
	</div>

	<!-- "Get in touch" button -->
	<a
		class="blueShadow group relative overflow-hidden rounded-full bg-white px-5 py-2 text-slate-950"
		href="#footer"
	>
		<!-- Background effect for button hover -->
		<div
			class="absolute right-full top-0 z-0 h-full w-full bg-violet-400 opacity-20 duration-200 group-hover:translate-x-full"
		></div>
		<!-- Button text -->
		<h4 class="z-9 relative">Get in touch!</h4>
	</a>
</header>
