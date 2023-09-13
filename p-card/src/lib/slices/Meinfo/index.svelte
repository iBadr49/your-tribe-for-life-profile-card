<script>
	/** @type {import("@prismicio/client").Content.MeinfoSlice} */
	export let slice;
</script>

<section data-slice-type={slice.slice_type} data-slice-variation={slice.variation}>
	Placeholder component for {slice.slice_type} (variation: {slice.variation}) Slices
</section>

<!-- met deze code kan je jouw prismic content zien -->
<pre>
	{JSON.stringify(slice, null, 2)}
</pre>