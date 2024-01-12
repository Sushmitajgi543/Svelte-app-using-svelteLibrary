<script>
	import { onMount } from 'svelte';

	let totalYears = 0;

	onMount(() => {
		const currentYear = new Date().getFullYear();
		const startYear = 2023;
		totalYears = currentYear - startYear + 1;
	});
</script>

<section>
	<h1>About Me</h1>
	<p>
		I am a Software Development Engineer with a passion for crafting innovative backend solutions.
		Hailing from Bihar and armed with a Master's in Computer Applications from ITM University, I
		bring over {totalYears} years of valuable experience to my role in a dynamic lab environment. My journey as
		a developer has been driven by a love for creating robust backend logics. I thrive on
		transforming ideas into functional, efficient code, continually seeking opportunities to learn
		and contribute to the ever-evolving tech landscape. My commitment to excellence and a keen
		interest in problem-solving define my approach to software development.
	</p>
</section>

