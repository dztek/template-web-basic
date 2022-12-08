<script>
	import Icon from 'ui/icon.svelte';

	let collapsed = false;
	
	function toggleMenu() {
		collapsed = !collapsed;
		alert('hi')
	}
</script>

<div class="layout-container" class:collapsed>
	<div class="sidenav">
		<div style="display:flex;align-items:flex-start;justify-content:flex-start;border:solid thick red;">
			webforma
		</div>
		<div>
			Content
		</div>
	</div>
	<main>
		<header>
		header
		</header>
		<div class="content">
			banner
		</div>
		<footer>
			footer
		</footer>
	</main>
</div>

<style>
	.layout-container.collapsed {
		grid-template-columns: 1fr 19fr;
	}
	.layout-container {
		display: grid;
		grid-template-columns: 1fr 3fr;
		border: solid thin;
		height: calc(100vh - 2em);
	}
	div.sidenav {
		display: flex;
		flex-direction: column;
		border: solid thin red;
		background: white;
	}
	header, footer {
		border: solid thick lime;
	}
	.content {
		border: solid thick skyblue;
	}
	.sidenav {
		display: grid;
	}
	main {
		border: solid thin blue;
		background: #cfcfcf;
		display: grid;
		grid-template-rows: 1fr 10fr 1fr;
	}
</style>