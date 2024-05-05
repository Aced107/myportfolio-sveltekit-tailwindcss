<!-- Importing the Step component -->
<script>
	import Step from './Step.svelte';

	// Array containing information about different projects
	let steps = [
		{
			name: 'Gymification',
			icon: 'fa-solid fa-dumbbell',
			href: 'https://gymification.netlify.app',
			ghref: 'https://github.com/Aced107/reactjs-tailwindcss-gymapp'
		},
		{
			name: 'NASA Picture of the Day',
			icon: 'fa-solid fa-rocket',
			href: 'https://apod-reactjs.netlify.app/',
			ghref: 'https://github.com/Aced107/reactjs-nasa-app'
		},
		{
			name: 'Todo App',
			icon: 'fa-solid fa-list-check',
			href: 'https://reactjs-tasklist.netlify.app/',
			ghref: 'https://github.com/Aced107/reactjs-todolist'
		}
	];

	// Array containing information about the benefits
	let benefits = [
		{
			name: 'a self taught developer',
			description:
				'I have been obsessed with coding ever since I was a teenager and decided to go down the route of making this my career. I learnt Python as my first programming language using online resources at the age of 16, and have ever since been diving deeper and deeper. My ever evolving knowledge ranges from JavaScript, HTML & CSS all the way to include JavaScript frameworks, backend programming, design, cloud services and much much more. My passion to widen my knowledge and skill set never ends.'
		},
		{
			name: 'product design & UX enthusiast',
			description:
				"I consider webpages my canvas, and the product design is my art. I am very strong at creating a unique branding for every webpage I create. Every bit of creativity I have gets poured into my work, and trust me, it's a never ending fountain"
		},
		{
			name: 'an excellent communicator',
			description:
				'I once read somewhere that communication is like a dance, and every interaction I have with someone solidifies that idea for me. I understand that communication is of the biggest factor that determines the success of a team/workplace environment and I do my best to use my communication skills to help develop deeper relations, and therefore boost the effectiveness and productivity of my workspace.'
		}
	];
</script>

<!-- Main section of the page -->
<main class="flex flex-1 flex-col p-4">
	<!-- Introduction section -->
	<section id="introPage" class="grid grid-cols-1 gap-10 py-8 sm:py-14 lg:grid-cols-3 lg:gap-0">
		<div
			class="flex flex-col gap-6 text-center md:gap-7 lg:col-span-2 lg:justify-center lg:gap-10 lg:text-left"
		>
			<!-- Introduction text -->
			<h2 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
				Hi! I'm <span class="poppins text-violet-400">Armaan</span> Mohammad <br />Full Stack
				<span class="poppins text-violet-400">Developer</span>
			</h2>
			<p class="text-base sm:text-lg md:text-xl">
				My favourite tech includes JavaScript (React.js or SvelteKit), TailwindCSS, Python + Django
				and Node.js + Express.js & PostgreSQL or Firebase/Firestore!
			</p>
			<!-- LinkedIn link -->
			<a
				class="blueShadow poppins group relative mx-auto overflow-hidden rounded-full bg-white px-6 py-3 text-base text-slate-950 sm:text-lg md:text-xl lg:ml-0 lg:mr-auto"
				href="https://www.linkedin.com/in/armaan-mohammad-365105235/"
				target="_blank"
			>
				<div
					class="absolute right-full top-0 z-0 h-full w-full bg-violet-400 opacity-20 duration-200 group-hover:translate-x-full"
				></div>
				<h4 class="z-9 relative">My LinkedIn &rarr;</h4>
			</a>
		</div>
		<!-- Image section -->
		<div class="relative grid place-items-center shadow-2xl lg:col-span-1">
			<img src="images/profile.png" alt="Zetane Engine" class="z-[2] max-h-[70vh] object-cover" />
		</div>
	</section>
	<!-- Projects section -->
	<section id="projects" class="flex flex-col gap-24 py-20 lg:py-32">
		<div class="flex flex-col gap-2 text-center">
			<h6 class="text-large sm:text-xl md:text-2xl">A Few Of My Creative Endeavors.</h6>
			<h3 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
				Curious to <span class="poppins text-violet-400">see</span> my work?
			</h3>
		</div>
		<!-- GitHub link -->
		<a
			href="https://github.com/Aced107"
			target="_blank"
			class="mx-auto -mb-4 -mt-10 flex items-center gap-2 rounded-md border border-solid border-white px-4 py-2 duration-200 hover:border-violet-700 sm:-mb-0"
		>
			<i class="fa-brands fa-github"></i>
			<p>Check my GitHub</p>
		</a>
		<!-- Individual project steps -->
		<div class="grid grid-cols-1 gap-12 lg:grid-cols-3 lg:gap-10">
			<Step step={steps[0]}>
				<!-- Information about the Gymification project -->
				<p>
					Gymification is The Ultimate Gym Training App built with <strong class="text-violet-400"
						>Reactjs & TailwindCSS</strong
					>
					hosted on <strong class="text-violet-400">Netlify</strong>
				</p>
			</Step>
			<Step step={steps[1]}>
				<!-- Information about the NASA Picture of the Day project -->
				<p>
					NASA APOD is a <strong class="text-violet-400">Reactjs</strong>
					frontend that consumes and caches the <strong class="text-violet-400">NASA API</strong> to
					generate a new astronomy picture every day and is also hosted on
					<strong class="text-violet-400">Netlify</strong>.
				</p>
			</Step>
			<Step step={steps[2]}>
				<!-- Information about the Todo App project -->
				<p>
					Todo is a <strong class="text-violet-400">Reactjs CRUD App</strong>
					that persists the task list on local storage, also hosted on
					<strong class="text-violet-400">Netlify</strong>
				</p>
			</Step>
		</div>
	</section>
	<!-- About me section -->
	<section
		id="about"
		class="lg:py32 relative flex flex-col gap-16 py-20 pt-10 sm:gap-20 md:gap-24 lg:pt-16"
	>
		<div
			class="relative flex flex-col gap-2 py-4 text-center before:absolute before:left-0 before:top-0 before:h-1.5 before:w-2/3 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:h-1.5 after:w-2/3 after:bg-violet-700"
		>
			<!-- Section heading -->
			<h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
			<h3 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
				A bit <span class="poppins text-violet-400">about</span> me
			</h3>
		</div>
		<!-- Introduction to the benefits section -->
		<p class="poppins mx-auto text-lg font-semibold sm:text-xl md:text-2xl">I am...</p>
		<!-- Looping through each benefit -->
		<div class="mx-auto flex w-full max-w-[800] flex-col gap-20">
			{#each benefits as benefit, index}
				<!-- Individual benefit section -->
				<div class="flex gap-6 sm:gap-8">
					<!-- Index number -->
					<p class="poppins text-4xl font-semibold text-slate-500 sm:text-5xl md:text-6xl">
						0{index + 1}
					</p>
					<div class="flex flex-col gap-6 sm:gap-8">
						<!-- Benefit name -->
						<h3 class="text-2xl sm:text-3xl md:text-5xl">{benefit.name}</h3>
						<!-- Benefit description -->
						<p>{benefit.description}</p>
					</div>
				</div>
			{/each}
		</div>
		<!-- Conclusion heading -->
		<h5 class="poppins text-center text-2xl font-semibold sm:text-3xl">
			The <span class="poppins text-violet-400">Complete</span> Package
		</h5>
		<!-- Comparison table -->
		<div class="mx-auto flex w-full max-w-[800px] flex-col gap-10 overflow-x-scroll">
			<table class="rounded bg-white text-center text-slate-700">
				<thead class="border-b border-solid border-slate-200"
					><tr class=""
						><th></th> <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
						<th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
						<th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
						<th class="whitespace-nowrap bg-violet-700 p-4 px-8 text-white">Me</th></tr
					></thead
				>
				<tbody
					><tr class="border-b border-solid border-slate-200"
						><td class="border-r border-solid border-white py-4 pl-4 pr-8 text-sm font-semibold"
							>Dedication</td
						> <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td></tr
					>
					<tr class="border-b border-solid border-slate-200"
						><td class="border-r border-solid border-white py-4 pl-4 pr-8 text-sm font-semibold"
							>Critical Thought</td
						> <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td></tr
					>
					<tr
						><td class="border-r border-solid border-white py-4 pl-4 pr-8 text-sm font-semibold"
							>Interpersonal Skills</td
						> <td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td></tr
					>
					<tr class="border-t border-solid border-slate-200"
						><td class="border-r border-solid border-white py-4 pl-4 pr-8 text-sm font-semibold"
							>Progamming Ability</td
						> <td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td></tr
					></tbody
				>
			</table>
		</div>
		<!-- Scroll indicator for small screens -->
		<div class="mx-auto -mt-12 italic opacity-50 sm:hidden">
			<p>Scroll to see more &rarr;</p>
		</div>
		<!-- Conclusion -->
		<p class="mx-auto">So why not Invest?</p>
	</section>
</main>
