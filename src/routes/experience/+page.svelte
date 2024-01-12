<script>
	// @ts-nocheck

	import Accordion from '../Accordion.svelte';
	import logion_logo from '../../lib/logion_solutions_logo.jpg'
	let show = null;
	const item = [
		{
			key: 'a',
			img: 'https://tts-website-images.s3.ap-south-1.amazonaws.com/onelab_logo.png',
			title: 'ONELAB VENTURES',
			des: 'SDE-1',
			subtitle: "JAN'23 - PRESENT",
			text: "Suppose you're moving toward a goal. You are, as they say, \"on the right path.\" But when you add the prefix un- you reverse that, and you're no longer on the path to that goal — you're untoward."
		},
		{
			key: 'b',
			img: 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAKYAAAAbCAMAAADBAgTuAAAAS1BMVEUAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADoIE/nIFAAAAAAAAAAAAASAgYAAAAAAAAAAAAAAAAAAAAAAAAAAADpIE7nIFAAAADpIE8S+Q/lAAAAF3RSTlMAIN+An7/vYJ8/QDCgEHCvUM+Qb49fIIpTcFIAAAHrSURBVFjDzdftUishDAbgQAp4YOl+eDTe/5VqEyHbLc4wTkf2/bO1bunTECgFyauBQxK08+/lDUblP9mDM9Ca28yPFxgQUdLBGYi+nOdiIlF1qpLInYq5EGfbFe/q+anrUKaJMYPGMinc3yJPmj6msVtZinapnaTTM1tJC+PKnEUepCQjV8q+6gS3Cpf4rksns96I+nEnMpVCjtNiVnzcv1uy5C+Is6+9aNnzsC9dWZ+fxJRrNzN5wswjb9/OuJtd3K8jx0Uew7Q6DMpK3rSYWNa7ltMNYQZ+WF8cS9FiY1/Kt798J3M2ku0XTCNZ1LaWl6rZlhY0nqpTm9b0MTVtpqTJpBJlkr8bfAUArVlSpw6e+pgrStwPzAunyfQomSrT3PcaWWHy9dE5czsM6E2G1WSuJtPg6NRqjmBaygwMC39JztqBd07POH6cRzCRUIa4XaWPJt0e2VmVSdphBDN7IYAjRLKN7TF5Vhb/PIQJgXxg70rkTd0eKarTpt3hIzyJeeF0MqV4DkPYfJ1px5P70IOTzPmTmJJ+JphJVglaivJv2VqbR2UceN7MMSzmNqu1T2+Z86PSnuH0bsIiVy+mBWpm4sQzMGuiMM3xUIyn+i0EEFS5c+LZfgBDskWpziucjgnGQG/eM/x9PgERlzISV/xU7QAAAABJRU5ErkJggg==',
			title: 'HIE-HQ',
			des: 'Software Developer',
			subtitle: "OCT'22 - DEC'22",
			text: "Suppose you're moving toward a goal. You are, as they say, \"on the right path.\" But when you add the prefix un- you reverse that, and you're no longer on the path to that goal — you're untoward."

		},
		{
			key: 'c',
			img: logion_logo,
			title: 'LOGION SOLUTIONS',
			des: 'Junior Web Developer',
			subtitle: "MAY'22 - SEPT'22",
			text: 'The journalist, who seems oddly unalarmed by the frequent reports of murders, loves a good chin-wag and keeps trying to chum up to Tshembe, who wants none of him.'
		},
		{
			key: 'c',
			img: 'https://www.zealousweb.com/wp-content/uploads/2022/08/Default.svg',
			title: 'ZEALOUSWEB TECHNOLOGY',
			des: 'Web Developer Intern',
			subtitle: "JAN'22 - APRIL'22",
			text: 'The journalist, who seems oddly unalarmed by the frequent reports of murders, loves a good chin-wag and keeps trying to chum up to Tshembe, who wants none of him.'
		},
		{
			key: 'c',
			img: 'http://www.autoclusteradityapur.com/wp-content/uploads/2019/02/adityapur-auto-cluster-logo.png',
			title: 'ADITYAPUR AUTOCLUSTER',
			des: 'Web Developer Intern',
			subtitle: "Dec'18 — Feb'19",
			text: 'The journalist, who seems oddly unalarmed by the frequent reports of murders, loves a good chin-wag and keeps trying to chum up to Tshembe, who wants none of him.'
		}
	];
	const showCollapse = (i) => {
		i === show ? (show = null) : (show = i);
	};
</script>

<svelte:head>
	<title>Experience</title>
</svelte:head>

<h1>Experience</h1>

<div class="accordion-container">
	{#each item as item, i}
		<Accordion {i} {show} {showCollapse} {item} />
	{/each}
</div>
