<script>
	// @ts-nocheck
	import { slide } from 'svelte/transition';

	export let i;
	export let show;
	export let showCollapse;
	export let item;
</script>

<button class="collapse__header" on:click={showCollapse(i)}>
	<div class="img">
		<img src={item.img} alt="Cover" />
	</div>
	<div>
		<h2>{item.des}</h2>
		<p>{item.subtitle}</p>
	</div>
</button>
{#if show === i}
	<div class="collapse__body" transition:slide>
		<p>
			{item.text}
		</p>
	</div>
{/if}

<style>
	.collapse__header {
		padding: 0.5rem;
		border: 1px solid grey;
		transition: background 200ms ease-in-out;
		width: 100%;
		display: flex;
		justify-content: flex-start;
		background-color: transparent;
		align-items: center;
	}
	.collapse__header:hover {
		background: #f7f7f7;
	}
	.collapse__body {
		padding: 1rem;
		background: #f0f0f0;
	}
	.collapse__header h2 {
		font-weight: 600;
	}
	.collapse__header p {
		font-weight: 300;
		font-size: 12px;
	}
	.collapse__header div {
		padding-left: 30px;
	}
	.img {
		width: 15%;
		border: 1px solid #f0f0f0;
		padding: 20px;
		background-color: rgba(240, 248, 255, 0.294);
	}
	.img img {
		width: 100%;
	}
</style>
