<script>
	let close = true;
	let path = 'M4 6h16v2H4zm0 5h16v2H4zm0 5h16v2H4z';
	function handlePath() {
		close = !close;
		if (close) {
			path = 'M4 6h16v2H4zm0 5h16v2H4zm0 5h16v2H4z';
		} else {
			path =
				'm16.192 6.344-4.243 4.242-4.242-4.242-1.414 1.414L10.535 12l-4.242 4.242 1.414 1.414 4.242-4.242 4.243 4.242 1.414-1.414L13.364 12l4.242-4.242z';
		}
	}
</script>

<div class="md:hidden">
	<svg
		xmlns="http://www.w3.org/2000/svg"
		width="30"
		height="30"
		viewBox="0 0 24 24"
		fill="#000"
		on:click={handlePath}
		on:keypress={handlePath}
		role="button"
		tabindex="0"><path d={path} /></svg
	>
</div>
