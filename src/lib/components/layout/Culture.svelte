<script lang="ts">
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import { animate, stagger } from "motion";
	import { onMount } from "svelte";

	// Types
	export type Value = {
		title: string;
		description: string;
	};

	// Props
	const { values = [] }: { values: Value[] } = $props();

	let cards: HTMLElement[] = $state([]);

	onMount(() => {
		if (!cards.length) return;
		if (window.self !== window.top) return;

		animate(
			cards,
			{
				y: ["1.5rem", 0],
				filter: ["blur(2px)", "blur(0px)"],
				opacity: [0, 1]
			},
			{
				duration: 0.3,
				ease: "easeOut",
				delay: stagger(0.1, {
					ease: "easeInOut"
				})
			}
		);
	});
</script>

<section class="bg-white dark:bg-gray-950">
	<div
		class="section-py section-px container mx-auto grid gap-8 [--gap:--spacing(8)] [--radius:var(--radius-2xl)]"
	>
		<SectionHeader title="Our culture." subtitle="The values that guide everything we do" />

  <div
    class="grid gap-(--gap)"
    style:grid-template-columns="repeat(auto-fit, minmax(280px, 1fr))"
  >
    <div bind:this={cards[0]} class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
      <div class="text-caption z-10">
        <div>
          <div class="text-headline mb-[1em]">Frontline first</div>
          <div class="text-body text-gray-500 dark:text-gray-400">We design with and for the operators who power industrial work. Every decision starts with the needs and realities of the shop floor.</div>
        </div>
      </div>
    </div>
    <div bind:this={cards[1]} class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
      <div class="text-caption z-10">
        <div>
          <div class="text-headline mb-[1em]">Clarity over complexity</div>
          <div class="text-body text-gray-500 dark:text-gray-400">We turn noisy information into clear, actionable guidance. Precision and simplicity matter—especially when safety and quality are on the line.</div>
        </div>
      </div>
    </div>
    <div bind:this={cards[2]} class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
      <div class="text-caption z-10">
        <div>
          <div class="text-headline mb-[1em]">Human connection, always</div>
          <div class="text-body text-gray-500 dark:text-gray-400">Remote-first doesn’t mean distant. We build a culture of trust, inclusivity, and growth—online and in person—so everyone can thrive.</div>
        </div>
      </div>
    </div>
    <div bind:this={cards[3]} class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
      <div class="text-caption z-10">
        <div>
          <div class="text-headline mb-[1em]">AI with purpose</div>
          <div class="text-body text-gray-500 dark:text-gray-400">We harness AI to turn expertise into repeatable action, but always as a tool to empower people—not replace them.</div>
        </div>
      </div>
    </div>
  </div>
		</div>
	</div>
</section>
