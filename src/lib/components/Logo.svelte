<script lang="ts">
	import type { HTMLAttributes } from "svelte/elements";
	const props: HTMLAttributes<SVGSVGElement> = $props();
</script>

<svg viewBox="0 0 120 40" fill="none" xmlns="http://www.w3.org/2000/svg" class="" {...props}>
  <!-- Squint Logo - Stylized "S" with eye motif -->
  <path d="M8 32C8 32 8 24 16 24C24 24 24 32 24 32C24 32 24 24 32 24C40 24 40 32 40 32" 
        stroke="currentColor" 
        stroke-width="3" 
        stroke-linecap="round" 
        fill="none"/>
  <circle cx="16" cy="20" r="4" fill="currentColor"/>
  <circle cx="32" cy="20" r="4" fill="currentColor"/>
  <circle cx="16" cy="20" r="1.5" fill="white"/>
  <circle cx="32" cy="20" r="1.5" fill="white"/>
  
  <!-- Squint Text -->
  <text x="52" y="28" font-family="var(--font-body)" font-size="24" font-weight="600" fill="currentColor">Squint</text>
</svg>

