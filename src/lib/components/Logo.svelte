<script lang="ts">
	import type { HTMLAttributes } from "svelte/elements";
	
	type Props = {
		class?: string;
		size?: number | string;
	} & HTMLAttributes<HTMLDivElement>;
	
	let { class: className = "", size = 32, ...props }: Props = $props();
</script>

<div class="flex items-center {className}" {...props}>
	<img 
		src="https://logo.clearbit.com/squint.ai" 
		alt="Squint" 
		class="w-auto"
		style="height: {typeof size === 'number' ? size + 'px' : size}"
	/>
</div>

