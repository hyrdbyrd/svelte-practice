<style>
	:global(body, html) {
		margin: 0;
		padding: 0;
	}

	:global(:root) {
		--primary-bg: #fc0;
		--secondary-bg: #ffd923;

		--transition: all linear .2s;
	}
</style>

<script lang="ts">
	import Slider from './components/Slider/Slider.svelte';
</script>

<Slider>
	<img src="/images/1.jpg" alt="1" />
	<img src="/images/2.jpg" alt="2" />
	<img src="/images/3.jpg" alt="3" />
	<img src="/images/4.jpg" alt="4" />
</Slider>

<Slider>
	<img src="/images/1.jpg" alt="1" />
	<img src="/images/2.jpg" alt="2" />
	<img src="/images/3.jpg" alt="3" />
	<img src="/images/4.jpg" alt="4" />
</Slider>
