<script>
	import { SliceZone } from '@prismicio/svelte';
	import { components } from '$lib/slices';
	export let data;
	console.log(data);
</script>

<!-- met deze code hieronder laat je je presmic.data zien op localhostpage -->
<!-- <SliceZone slices={data.slices} {components} /> -->

<div class="profile-card">
	<h1>{data.slices[0].primary.naam[0].text}</h1>
	<p>{data.slices[0].primary.text[0].text}</p>
	<p>{data.slices[0].primary.text2[0].text}</p>
	<p>{data.slices[0].primary.text3[0].text}</p>
</div>

<style>
	:global(body) {
		background-color: #000000;
	}
	.profile-card {
		background-color: #ffffff;
		box-shadow: 0 4px 6px #FB3640;
		padding: 20px;
		margin: 50px;
		border-radius: 8px;
	}
</style>
