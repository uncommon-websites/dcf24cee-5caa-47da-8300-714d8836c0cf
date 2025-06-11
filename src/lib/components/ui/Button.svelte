<script lang="ts">
	// Types
	import type { Snippet } from "svelte";
	import type { ButtonRootProps } from "bits-ui";
	import { Button } from "bits-ui";

	type Variant = "primary" | "secondary" | "ghost";
	type Size = "sm" | "md" | "lg";

	type Props = ButtonRootProps & {
		variant?: Variant;
		size?: Size;
		children: Snippet;
		iconOnly?: boolean;
		hideLabel?: boolean;
		rounded?: boolean;
		prefix?: Snippet;
		suffix?: Snippet;
	};

	// Props
	const {
		variant = "primary",
		size = "md",
		children,
		class: classes = "",
		prefix: Prefix,
		suffix: Suffix,
		iconOnly = false,
		hideLabel = false,
		...rest
	}: Props = $props();

	// Styles
	const variants: Record<Variant, string> = {
		primary: "bg-primary text-primary-foreground hover:bg-primary/90",
		secondary: "bg-secondary text-secondary-foreground hover:bg-secondary/80",
		ghost: "hover:bg-accent hover:text-accent-foreground"
	};

	const sizes: Record<Size, string> = $derived({
		sm: iconOnly ? "p-1.5 text-caption" : "px-4 py-1.5 rounded text-caption",
		md: iconOnly ? "p-2 text-body" : "px-4.5 py-2 rounded text-body",
		lg: iconOnly ? "p-2.5 text-headline" : "px-5 py-2 rounded-lg text-headline"
	});

	const baseStyles =
		"inline-flex items-center ring-1 ring-white/15 ring-inset justify-center !font-semibold transition ease-out duration-300 focus:outline-none focus:ring-2 focus:ring-ring focus:ring-offset-2 active:brightness-[.9] active:scale-[.98] gap-3 [touch-action:manipulation] rounded-md";
</script>

<Button.Root
	{...rest}
	class={[
		baseStyles,
		variants[variant],
		iconOnly && "aspect-square",
		sizes[size],
		"gap-2",
		classes
	]}
	data-variant={variant}
	data-size={size}
>
	{#if Prefix}
		<Prefix />
	{/if}
	<span class:sr-only={hideLabel || iconOnly}>
		{@render children?.()}
	</span>
	{#if Suffix}
		<Suffix />
	{/if}
</Button.Root>
