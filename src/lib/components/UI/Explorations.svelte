<script lang="ts">
</script>

<div class="explore_card">
	<div class="explore_title">
		<h1>
			<a href="/explorations">lorem</a>
		</h1>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			width="16"
			height="16"
			viewBox="0 0 24 24"
			fill="none"
			stroke="currentColor"
			stroke-width="2"
			stroke-linecap="round"
			stroke-linejoin="round"
			class="heading"
			><path d="M15 3h6v6" /><path d="M10 14 21 3" /><path
				d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"
			/></svg
		>
	</div>
	<p class="explore_description">Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
</div>

<style>
	.explore_title {
		display: flex;
		align-items: center;
		gap: 0.25rem;
	}

	.explore_title h1 {
		margin-bottom: 0.35rem;
		cursor: pointer;
		text-transform: capitalize;
		font-weight: 500;
		position: relative;
		overflow: hidden;
	}

	.explore_title h1::before,
	.explore_title h1::after {
		content: '';
		position: absolute;
		bottom: 0px;
		left: 0%;
		height: 1px;
		background: var(--paragraph-colour);
		transition: all 0.5s ease;
	}

	.explore_title h1::before {
		left: 0;
		width: 100%; /* Full width initially */
	}

	.explore_title h1::after {
		right: 0;
		width: 0%; /* Hidden initially */
		transition-delay: 0.1s;
	}

	.explore_title h1:hover::before {
		width: 0%; /* Shrinks away */
		left: 100%; /* Moves to the right, effectively disappearing */
	}

	.explore_title h1:hover::after {
		width: 100%; /* Grows to full width */
		right: 0; /* Starts growing from the left */
	}

	.explore_title svg {
		transform: translateY(-3px);
	}

	.explore_description {
		font-size: 0.85rem;
		line-height: 1.65;
	}
</style>
