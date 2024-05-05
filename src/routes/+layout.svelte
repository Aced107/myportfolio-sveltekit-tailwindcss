<!-- 
    This is the layout component of the web application. It serves as a template for the overall structure 
    of each page. It imports global styles and other components required for the layout.
-->

<script>
	// Importing the global CSS file and necessary components
	import '../app.css';
	import Footer from '../components/Footer.svelte';
	import Header from '../components/Header.svelte';

	// Declaring variables to store scroll position and window dimensions
	let y; // Vertical scroll position
	let innerHeight = 0; // Height of the window's content area
	let innerWidth = 0; // Width of the window's content area

	// Function to scroll to the top of the page
	function goTop() {
		document.body.scrollIntoView();
	}
</script>

<!-- 
    The main layout structure using flexbox. 
    It ensures that the content occupies the entire height of the screen.
    The maximum width of the content is restricted to 1400px.
-->
<div class="realtive mx-auto flex min-h-screen w-full max-w-[1400px] flex-col text-sm sm:text-base">
	<!-- 
        This div contains the scroll-to-top button.
        It is initially hidden and becomes visible when the user scrolls down.
    -->
	<div
		class={'fixed bottom-0 z-[10] flex w-full p-10 duration-200 ' +
			(y > 0 ? 'opacity-full pointer-events-auto' : 'pointer-events-none opacity-0')}
	>
		<button
			on:click={goTop}
			class="ml-auto grid aspect-square cursor-pointer place-items-center rounded-full bg-slate-900 px-3 text-violet-400 hover:bg-slate-800 sm:px-4"
		>
			<i class="fa-solid fa-arrow-up grid aspect-square place-items-center"></i>
		</button>
	</div>

	<!-- 
        Including the Header component and passing the scroll position as a prop.
        The Header component contains the navigation menu.
    -->
	<Header {y} />

	<!-- 
        This slot is where the content of each page will be placed.
        The actual content will be rendered inside this slot.
    -->
	<slot />

	<!-- 
        Including the Footer component.
        The Footer component contains information such as copyright, contact details, etc.
    -->
	<Footer />
</div>

<!-- 
    Binding the scroll position, innerHeight, and innerWidth to the window object.
    This ensures that these variables are updated whenever the corresponding window properties change.
-->
<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
