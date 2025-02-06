<script lang="ts">
	import { onMount } from 'svelte';
	import { cubicIn, cubicOut } from 'svelte/easing';
	import { fade } from 'svelte/transition';

	let { item } = $props() as { item: { title: string; price: number; description: string } };

	onMount(() => {
		console.log(item);
	});
</script>

<div class="box" in:fade={{ delay: 500, duration: 5000 }}>
	{item.title}
	{item.price}
</div>
