<script>
	import { onMount } from "svelte";
	import Header from "./Header.svelte";
	import AboutMe from "./AboutMe.svelte";
	import Experiences from "./Experiences.svelte";
	import Achievements from "./Achievements.svelte";
	import Projects from "./Projects.svelte";
	import Footer from "./Footer.svelte";

	let isDarkMode = true;
	let showButton = false;

	function toggleTheme() {
		isDarkMode = !isDarkMode;
		document.body.classList.toggle("light-mode", !isDarkMode);
		document.body.classList.toggle("dark-mode", isDarkMode);
	}

	function scrollToTop() {
		window.scrollTo({ top: 0, behavior: "smooth" });
	}

	function checkScroll() {
		showButton = window.scrollY > 100;
	}

	function openLink() {
		window.open(
			"https://drive.google.com/file/d/13l0zz4Ko3mK5FsZx6WJLnIFUNcqxSU2_/view",
			"_blank",
		);
	}

	onMount(() => {
		if (
			window.matchMedia &&
			window.matchMedia("(prefers-color-scheme: light)").matches
		) {
			isDarkMode = false;
			document.body.classList.add("light-mode");
		}
		window.addEventListener("scroll", checkScroll);
		return () => {
			window.removeEventListener("scroll", checkScroll);
		};
	});
</script>

<div class="container">
	<Header />
	<AboutMe />
	<Experiences />
	<Achievements />
	<Projects />
	<Footer />

	<button class="resume" on:click={openLink}>Resume</button>

	<button class="toggle-theme" on:click={toggleTheme}>
		{isDarkMode ? "Light Mode" : "Dark Mode"}
	</button>

	<button
		class="top-button {showButton ? 'visible' : ''}"
		on:click={scrollToTop}
	>
		<svg
			viewBox="0 0 24 24"
			width="24"
			height="24"
			fill="none"
			stroke="currentColor"
			stroke-width="2"
			stroke-linecap="round"
			stroke-linejoin="round"
		>
			<path d="M18 15l-6-6-6 6"></path>
		</svg>
	</button>
</div>

<style>
	:global(body) {
		font-family: "Sans-serif", sans-serif;
		margin: 0;
		padding: 0;
		transition:
			background-color 0.3s,
			color 0.3s;
	}

	:global(.light-mode) {
		background-color: #f4f4f4;
		color: #333;
	}

	:global(.dark-mode) {
		background-color: #f4f4f4;
		color: white;
	}

	.container {
		margin: 0 auto;
		background-color: var(--container-bg);
		box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
		transition: background-color 0.3s;
	}

	:global(.light-mode) .container {
		background-color: #ffffff;
	}

	.toggle-theme {
		position: absolute;
		top: 20px;
		right: 20px;
		background: none;
		border: 2px solid var(--highlight-color);
		color: var(--highlight-color);
		padding: 10px;
		border-radius: 5px;
		cursor: pointer;
		transition:
			background-color 0.3s,
			color 0.3s;
	}

	:global(.light-mode) .toggle-theme {
		border-color: #333;
		color: #333;
	}

	.resume {
		position: absolute;
		top: 20px;
		left: 20px;
		background: none;
		border: 2px solid var(--highlight-color);
		color: var(--highlight-color);
		padding: 10px;
		border-radius: 5px;
		cursor: pointer;
		transition:
			background-color 0.3s,
			color 0.3s;
	}

	:global(.light-mode) .resume {
		border-color: #333;
		color: #333;
	}

	:root {
		--container-bg: #1e1e1e;
		--highlight-color: #61dafb;
		--subheading-color: #9b9b9b;
		--border-color: #333;
	}

	:global(.light-mode) {
		--container-bg: #ffffff;
		--highlight-color: #007acc;
		--subheading-color: #666;
		--border-color: #ccc;
	}

	.top-button {
		position: fixed;
		bottom: 20px;
		right: 20px;
		width: 50px;
		height: 50px;
		border-radius: 50%;
		background-color: #007bff;
		color: white;
		border: none;
		cursor: pointer;
		display: flex;
		align-items: center;
		justify-content: center;
		opacity: 0;
		transition: opacity 0.3s;
	}

	.top-button.visible {
		opacity: 1;
	}
</style>
