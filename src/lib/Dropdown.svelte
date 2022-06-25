<script>
	export let title;
	let show = false;
	export let last = false;
</script>

<!-- svelte-ignore a11y-mouse-events-have-key-events -->
<div
	class="drop"
	on:mouseleave={() => {
		show = false;
	}}
	on:mouseover={() => {
		show = true;
	}}
>
	<h2>
		{title}
	</h2>
	<div class:no={!show} class="menu" class:last>
		<slot />
	</div>
</div>

<style>
	.drop {
		position: relative;
	}
	.menu {
		position: absolute;
		border-radius: 10px;
		transition: display ease;
		z-index: 20;
	}
	.no {
		display: none;
	}
	* {
		white-space: nowrap;
	}
	.last {
		position: absolute;
		right: 0;
	}
	h2:hover {
		color: #efefef;
	}
</style>
