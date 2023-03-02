<script>
	export let id, title, subtitle, content, author, featuredImage;
</script>

<div class="card">
	<div class="card__top">
		<img src={featuredImage} />

		<div class="card__titles">
			<h1 class="card__title">
				{title};
			</h1>
		</div>
		<div class="card__bottom">
			<div class="card__content">
				<p>
					{content}
				</p>
			</div>
			<div class="card__author">
				<p>{author}</p>
			</div>
		</div>
	</div>
</div>

<style>
	.card {
		display: flex;
		flex-direction: column;
		height: 100%;
		align-items: center;
	}
	.card__title {
		font-size: 1.24rem;
	}
</style>
