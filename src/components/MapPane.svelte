<script>
	import { onMount } from 'svelte';
	import Section from './Section.svelte';
	import mapboxgl from 'mapbox-gl';
	import 'mapbox-gl/dist/mapbox-gl.css';

	let mapContainer;

	let map;

	onMount(() => {
		mapboxgl.accessToken =
			'pk.eyJ1IjoiY3lmaW5mYXphIiwiYSI6ImNrYXBwN2N4ZTEyd3gycHF0bHhzZXIwcWEifQ.8Dx5dx27ity49fAGyZNzPQ';
		const map = new mapboxgl.Map({
			container: mapContainer,
			style: 'mapbox://styles/cyfinfaza/clerkfmgw002701o13qf06k87', // style URL
			center: [-74.5465931, 40.6948376],
			zoom: 18
		});
	});
</script>

<Section id="map">
	<div class="mapContainer" bind:this={mapContainer} />
	<h1>Map</h1>
</Section>

<style lang="scss">
	:global(.section#map) {
		position: relative;
		height: 400px;
		overflow: hidden;
		justify-content: unset;
	}
	.mapContainer {
		position: absolute;
		inset: 0;
	}
	:not(.mapContainer) {
		z-index: 5;
		position: relative;
	}
</style>
