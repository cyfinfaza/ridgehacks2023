<script>
	import { onMount } from 'svelte';
	import Section from './Section.svelte';
	import mapboxgl from 'mapbox-gl';
	import 'mapbox-gl/dist/mapbox-gl.css';

	let mapContainer;

	let map;

	onMount(() => {
		mapboxgl.accessToken =
			'pk.eyJ1IjoicmlkZ2Vjb21wc2NpIiwiYSI6ImNsZXJrcW5oODB5MDI0M3Rra3YzMXJmNzAifQ.92W1OyJckS4MCg0DCwqxXg';
		const map = new mapboxgl.Map({
			container: mapContainer,
			style: 'mapbox://styles/ridgecompsci/clerkqzw9002h01r31zzvxvh0', // style URL
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
