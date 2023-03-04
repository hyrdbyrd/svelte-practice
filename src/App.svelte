<style>
	:global(body, html) {
		margin: 0;
		padding: 0;

		max-height: 100vh;
		max-width: 100vw;
	}

	:global(:root) {
		--primary-bg: #fc0;
		--secondary-bg: #ffd923;

		--transition: all linear .2s;
	}

	div {
		display: flex;
		align-items: center;
		justify-content: center;

		padding: 100px;
	}
</style>

<script lang="ts">
	import Slider from './components/Slider/Slider.svelte';
</script>

<div>
	<Slider>
		<img src="/images/1.jpg" alt="1" />
		<img src="/images/2.jpg" alt="2" />
		<img src="/images/3.jpg" alt="3" />
		<img src="/images/4.png" alt="4" />
		<img src="/images/5.png" alt="5" />
	</Slider>
</div>
