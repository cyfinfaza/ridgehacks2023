<script>
	export let id;
</script>

<div class="section" {id}>
	<div>
		<slot />
	</div>
</div>

<style lang="scss">
	.section {
		// height: calc(100vh - var(--section-spacing) * 2);
		width: 100%;
		max-width: var(--width);
		border-radius: calc(0.75 * var(--section-spacing));
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding-top: 32px;
		padding-bottom: 32px;
		// margin-top: var(--section-spacing);
		// margin-bottom: var(--section-spacing);
		font-size: 1.2em;
		p {
			line-height: 1.3em;
		}
		// transform: translateY(20px) rotate(-3deg);
		// text-align: center;
		color: var(--text);
		h1 {
			font-size: 3rem;
		}
		> :global(*) {
			max-width: min(100%, var(--width));
			> :global(*) {
				padding-left: 32px;
				padding-right: 32px;
			}
		}
		> :global(*) {
			width: var(--width);
			max-width: 100%;
		}
		scroll-margin-top: calc(0.5 * var(--logo-height) + 1.5 * var(--section-spacing));
	}
</style>
