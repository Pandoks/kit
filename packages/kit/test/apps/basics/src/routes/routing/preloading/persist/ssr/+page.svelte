<script>
	/** @type {{ data: { calls: number } }} */
	let { data } = $props();
</script>

<p data-testid="load-calls">{data.calls}</p>
