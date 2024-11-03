<script lang="ts">
	interface CardProps {
		name: string;
		cientificName: string;
		origin: string;
		src: string;
	}
	const { name, cientificName, origin, src }: CardProps = $props();

	import { strings } from './card.strings';
</script>

<div>
	<img {src} alt={name} />
	<h2>{name}</h2>
	<p>{strings.cientificName} {cientificName}</p>
	<p>{strings.origin}{origin}</p>
</div>

<style>
	div {
		border: 1px solid #ccc;
		display: flex;
		flex-direction: column;
		border-radius: 4px;
		padding: 1rem;
		max-width: 300px;
		max-height: 400px;
		border-radius: 8px;
		transition-duration: 500ms;
		&:hover {
			box-shadow: 0 10px 10px rgba(0, 0, 0, 0.1);
			cursor: pointer;
		}
	}

	img {
		width: 100%;
		border-radius: 4px;
	}
</style>
