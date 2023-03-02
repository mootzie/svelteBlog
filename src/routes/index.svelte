<script>
	import { onMount } from 'svelte';
	import Header from '../components/Header.svelte';
	import Card from '../components/Card.svelte';
	import Container from '../components/Container.svelte';

	export let posts = [];
	let endPoint = 'http://next-blog.local/wp-json/wp/v2/posts';

	onMount(() => {
		fetch(endPoint)
			.then((response) => response.json())
			.then((result) => (posts = result));
	});
</script>

<Container>
	<Header />
	{#if posts}
		{#each posts as post (post.id)}
			<Card
				title={post.title}
				content={post.content}
				author={post.author}
				featuredImage={post.featuredImage}
			/>
		{/each}
	{/if}
</Container>

<style>
	* {
		padding: 0;
		margin: 0;
	}
	.main {
		padding: 0;
		margin: 0;
	}
</style>
