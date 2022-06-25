<script>
	let showInfo = false;
</script>

<div class="card">
	<img src="https://upload.wikimedia.org/wikipedia/commons/0/05/HONDA_ASIMO.jpg" alt="" />
	<div class="bottom">
		<div class="txt">
			<h1>Robot</h1>
			<h2>$100</h2>
		</div>
		<div class="cart" on>
			<h1><i class="bi bi-cart-plus-fill" /></h1>
		</div>
	</div>
	<!-- svelte-ignore a11y-mouse-events-have-key-events -->
	<div
		class="infoClick"
		on:mouseover={() => {
			showInfo = !showInfo;
		}}
		class:no={showInfo}
	>
		<h2>&nbsp;<i class="bi bi-info-circle" /></h2>
	</div>
	<div
		class="info"
		on:mouseleave={() => {
			showInfo = !showInfo;
		}}
		class:no={!showInfo}
	>
		<h3>
			Lorem ipsum dolor, sit amet consectetur adipisicing elit. Eos quod, hic in recusandae nemo
			officiis nam nulla porro nostrum possimus?
		</h3>
	</div>
</div>

<style>
	img {
		width: 100%;
		height: 250px;
		object-fit: cover;
		border-radius: 5px 5px 0 0;
	}
	.no {
		transform: scale(0);
	}
	.card {
		background-color: #127a94;
		width: max-content;
		border-radius: 5px;
		position: relative;
		margin: 1em;
		flex-grow: 1;
		max-width: 300px;
	}
	.card:hover {
		margin-top: 0.5em;
		transition: margin-top 0.3s;
	}
	.bottom {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}
	.txt {
		padding: 0 0.5em;
	}
	.cart {
		padding: 1em;
		border-left: 1px solid #25b6db;
		background-color: #007291;
	}
	.infoClick {
		position: absolute;
		right: 0;
		top: 0;
		background-color: #eba057;
		padding: 0.2em 0.5em;
		border-radius: 0 5px 0 60%;
	}
	.info {
		position: absolute;
		top: 0;
		background: #eba057;
		font-weight: 300;
		padding: 0.2em;
		transition: all 0.2s ease-in-out;
		border-radius: 5px 5px 0 0;
		min-height: 250px;
	}
</style>
