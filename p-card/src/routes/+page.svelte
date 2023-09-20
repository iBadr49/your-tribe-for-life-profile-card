<script>
	import { SliceZone } from '@prismicio/svelte';
	import { components } from '$lib/slices';
	export let data;
	console.log(data);
</script>

<!-- met deze code hieronder laat je je presmic.data zien op localhostpage -->
<!-- <SliceZone slices={data.slices} {components} /> -->

<section class="profile-card">
	<div class="image">
		<img src={data.slices[0].primary.image.url} />
	</div>
	<div class="text">
		<h1>{data.slices[0].primary.naam[0].text}</h1>
		<p>{data.slices[0].primary.text[0].text}</p>
		<p>{data.slices[0].primary.text2[0].text}</p>
		<p id="email">{data.slices[0].primary.text3[0].text}</p>
	</div>
</section>

<style>
	.profile-card {
		display: flex;
		align-items: center;
		margin: 50px;
		padding: 20px;
	}

	img {
		height: 200px;
		width: auto;
	}

	.image {
		margin-right: 10px;
	}

	.text {
		display: flex;
		flex-direction: column;
	}
</style>
