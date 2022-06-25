<script>
	import Dropdown from '../lib/Dropdown.svelte';
	import Item from '../lib/Item.svelte';
</script>

<div class="shop">
	<div class="filter">
		<Dropdown title="Featured">
			<h3 class="dropItem first">New Release</h3>
			<h3 class="dropItem">Best Seller</h3>
			<h3 class="dropItem last">All Items</h3>
		</Dropdown>
		<Dropdown title="Inventions">
			<h3 class="dropItem first">Robots</h3>
			<h3 class="dropItem">Guns</h3>
			<h3 class="dropItem last">All Inventions</h3>
		</Dropdown>
		<Dropdown title="Build Kits">
			<h3 class="dropItem first">Physics</h3>
			<h3 class="dropItem">Chemistry</h3>
			<h3 class="dropItem">Robotics</h3>
			<h3 class="dropItem last">All Kits</h3>
		</Dropdown>
		<Dropdown title="Apparel" last="true">
			<h3 class="dropItem first">Lab Clothes</h3>
			<h3 class="dropItem">Dexter Picks</h3>
			<h3 class="dropItem last">All Clothes</h3>
		</Dropdown>
	</div>
	<div class="cart" />
	<div class="items">
		<Item />
	</div>
</div>

<style>
	.shop {
		background-color: #232626;
	}
	.filter {
		display: flex;
		background-color: #007291;
		justify-content: space-between;
		margin: 1.5em;
		padding: 0.3em 0.7em;
		border-radius: 5px;
		cursor: default;
	}

	.dropItem {
		background-color: #eba057;
		padding: 0.3em 0.5em;
		z-index: 20;
	}
	.dropItem:hover {
		background-color: #d18c46;
	}
	.first {
		border-top-right-radius: 5px;
		border-top-left-radius: 5px;
	}
	.last {
		border-bottom-right-radius: 5px;
		border-bottom-left-radius: 5px;
	}
	.items {
		padding: 1em 2em;
	}
</style>
