<script lang="ts">
	import { formatDate } from '$lib/utils/utils';

	export let title: string;
	export let subtitle: string;
	export let _createdAt: string;
	export let slug: string;
</script>

<a href={`papers/${slug}`} class="container">
	<div class="heading">
		<h3>{title}</h3>
		<p>{subtitle}</p>
	</div>
	<p class="date">{formatDate(_createdAt)}</p>
</a>

<style>
	.container {
		cursor: pointer;
		padding: 1rem 0rem;
		display: flex;
		align-items: start;
		justify-content: space-between;
		border-top: 1px solid var(--paragraph-colour);
	}

	h3 {
		text-transform: capitalize;
		margin-bottom: 0.5rem;
	}
	.container:hover {
		background: #ebebeb9a;
	}
	
	@media (prefers-color-scheme: dark) {
		.container:hover {
			background: #4d4c4c9a;
		}
	}
</style>
