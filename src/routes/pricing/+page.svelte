<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Marco Rivera",
      position: "Manufacturing Process Lead",
      company: "Orion Components",
      quote:
        "We saw a return on investment within the first quarter. Squint made it easy for our line operators to adapt, and our error rates dropped by more than 40%.",
      image: "/generated/image-a-professional-headshot-of-a-latino-man-.webp"
    },
    {
      name: "Aisha Mbaye",
      position: "Assembly Operations Manager",
      company: "Velocity AutoWorks",
      quote:
        "I can train new hires in days instead of weeks. Squint eliminated confusion and keeps our teams on the same page—no matter the shift.",
      image: "/generated/image-a-professional-headshot-of-a-black-woman.webp"
    },
    {
      name: "Wei Zhou",
      position: "Field Operations Director",
      company: "Helio Energy Solutions",
      quote:
        "Deploying Squint was seamless. The intuitive interface won over field operators instantly, and our onboarding costs fell by a third.",
      image: "/generated/image-a-professional-headshot-of-an-east-asian.webp"
    }
  ]}
/>

<CallToAction
  title="Train faster. Work smarter. Fix it on the first try."
  subtitle="Squint turns your existing training material into step-by-step spatial procedures any operator can follow—right from their phone or tablet."
  description="Ready to boost productivity and compliance? See how industry leaders use Squint to cut training time and get results that stick."
  imageSrc="/generated/image-a-happy-industrial-worker-in-a-manufactu.webp"
  callsToAction={[
    { href: '/demo', label: 'Request a demo', variant: 'primary' },
    { href: '/contact', label: 'Talk to sales', variant: 'secondary' }
  ]}
/>
