<script>
	import { onMount } from 'svelte';
	import Section from './Section.svelte';
	import mapboxgl from 'mapbox-gl';
	import 'mapbox-gl/dist/mapbox-gl.css';

	let mapContainer;

	let map;

	onMount(() => {
		mapboxgl.accessToken =
			'pk.eyJ1IjoiYWxwaG9uc2U1IiwiYSI6ImNrcGU2YnJvODFrcHMycHBnMTZ3NWQ2d3EifQ.6giPwg07RZdYWFEvdYe32A';
		const map = new mapboxgl.Map({
			container: mapContainer,
			style: 'mapbox://styles/alphonse5/cleqda8m0003y01qlfhr22bgh', // style URL
			center: [-74.5465931, 40.6948376],
			zoom: 18
		});
		const geolocate = new mapboxgl.GeolocateControl({
			positionOptions: {
				enableHighAccuracy: true
			},
			trackUserLocation: true,
			showUserHeading: true
		});
		map.addControl(geolocate);
		const navigation = new mapboxgl.NavigationControl();
		map.addControl(navigation);
		map.scrollZoom.disable();
	});
</script>

<Section id="map">
	<div class="mapContainer" bind:this={mapContainer} />
	<h1>Map</h1>
	<!-- <button>Re-Center</button> -->
</Section>

<style lang="scss">
	:global(.section#map) {
		position: relative;
		height: 450px;
		overflow: hidden;
		justify-content: unset;
	}
	:global(.mapboxgl-control-container) {
		position: static;
		z-index: 10;
		width: 100%;
	}
	.mapContainer {
		position: absolute;
		inset: 0;
	}
	:not(.mapContainer) {
		z-index: 5;
		position: relative;
		text-shadow: 0 0 5px black;
	}
	h1 {
		align-self: flex-start;
		pointer-events: none;
	}
</style>
