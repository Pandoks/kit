<script>
	/** @type {{ data: { base: number, mutations?: number } }} */
	let { data } = $props();
	data.mutations = (data.mutations ?? 0) + 1;
</script>

<p data-testid="mutations">{data.mutations}</p>
