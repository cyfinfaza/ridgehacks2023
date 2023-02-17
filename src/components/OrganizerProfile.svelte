<script>
	export let fullName, role, image;
</script>

<div class="organizer">
	<img src={'/organizers/' + image} alt={fullName} />
	<div class="organizerInfo">
		<h3>{fullName}</h3>
		<p>{role}</p>
	</div>
</div>

<style lang="scss">
	.organizer {
		display: flex;
		align-items: center;
		gap: 16px;
		height: 100%;

		img {
			height: 100px;
			aspect-ratio: 1 / 1;
			object-fit: cover;
			border-radius: 50%;
		}

		.organizerInfo {
			display: flex;
			flex-direction: column;
			gap: 8px;
			> * {
				margin: 0;
			}
			// > *:nth-child(2) {
			// 	opacity: 0.7;
			// }
		}
	}
</style>
