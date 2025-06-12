<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";

	// Icons
	import IconBrain from "~icons/lucide/brain";
	import IconVideo from "~icons/lucide/video";
	import IconMapPin from "~icons/lucide/map-pin";
	import IconBadge from "~icons/lucide/badge";
	import IconBarChart from "~icons/lucide/bar-chart";
	import IconMessageCircle from "~icons/lucide/message-circle";
</script>

<CustomerCardHero
	centered={true}
	title="Empower every operator."
	subtitle="Turn your existing docs, photos, and videos into clear, step-by-step procedures your frontline teams can follow—on the floor, in real time."
	customers={[
		{
			name: "Jerrod Simpson",
			position: "Training Coordinator, Pall Corporation",
			imageSrc: "/generated/image-a-cheerful-woman-industrial-manager-wear.webp"
		},
		{
			name: "Rachel",
			position: "Learning & Development, Siemens",
			imageSrc: "/generated/image-a-young-woman-food-and-beverage-supervis.webp"
		},
		{
			name: "Darryl Brooks",
			position: "Senior Field Operator, Texas Oil & Gas",
			imageSrc: "/generated/image-a-middle-aged-man-in-an-oil-and-gas-unif.webp"
		},
		{
			name: "Wei Zhang",
			position: "Lead Engineer, Midwest Automotive",
			imageSrc: "/generated/image-an-asian-senior-male-engineer-in-an-auto.webp"
		},
		{
			name: "Latoya Green",
			position: "QA Supervisor, Modern Manufacturing",
			imageSrc: "/generated/image-a-black-female-quality-assurance-supervi.webp"
		}
	]}
	callsToAction={[
		{ href: "/demo", label: "Request a demo" },
		{ href: "/contact", label: "Contact sales" }
	]}
/>
<LogoScroller label="" />

<Summary
	title="AI-powered procedures for the industrial front line"
	text="Squint turns your existing videos, spreadsheets, and PDFs into step-by-step augmented reality procedures your operators can actually follow. Standardize work, deliver on-the-job help, and get real operational insights—all in one platform."
/>

<Testimonials
	testimonials={[
		{
			name: "Jerrod Griffin",
			position: "Training Coordinator, Automotive Plant",
			company: undefined,
			quote:
				"With Squint, we've cut training time by 40% and had new hires running independently in under a week.",
			image: "/generated/image-a-male-plant-manager-in-an-automotive-fa.webp"
		},
		{
			name: "Rachel Nuñez",
			position: "Learning & Safety, Food Production Facility",
			company: undefined,
			quote:
				"We went from monthly safety issues to zero reported incidents in two sites. Squint ensures nothing gets skipped.",
			image: "/generated/image-a-female-line-supervisor-on-a-food-produ.webp"
		},
		{
			name: "Kai Morrison",
			position: "Field Ops Supervisor, Offshore Oil Rig",
			company: undefined,
			quote:
				"Using Squint cut procedural rework and contractor retraining costs by over $85,000 last quarter alone.",
			image: "/generated/image-a-male-oil-rig-supervisor-standing-outsi.webp"
		}
	]}
/>

<Features
	title="Features built for frontline excellence"
	subtitle="AI-powered instructions, real-time help, and unmatched control—designed for operations that can’t skip a beat."
	features={[
		{
			title: "AI-powered step-by-step procedures",
			description:
				"Squint transforms your videos, PDFs, and manuals into clear, interactive guidance every operator can follow.",
			icon: IconBrain
		},
		{
			title: "Instant video-to-procedure conversion",
			description:
				"Turn any how-to video into a repeatable procedure in seconds. Capture knowledge the moment it's shared.",
			icon: IconVideo
		},
		{
			title: "Pin steps to the real world",
			description:
				"Attach vital instructions, notes, or content to where the work happens—no QR codes or special hardware needed.",
			icon: IconMapPin
		},
		{
			title: "Operator badge login",
			description:
				"Frontline teams access procedures securely and instantly with a simple badge scan—no passwords to remember.",
			icon: IconBadge
		},
		{
			title: "Real-time floor analytics",
			description:
				"Track operator activity, compliance, and training gaps as they happen. Take quick action where it matters.",
			icon: IconBarChart
		},
		{
			title: "Instant answers for every shift",
			description:
				"Operators get quick, accurate guidance on the job—no need to dig through docs or wait for a supervisor.",
			icon: IconMessageCircle
		}
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world applications for your business needs"
	useCases={[
		{
			title: "Accelerated onboarding for new operators",
			description:
				"Train new frontline workers in days, not weeks. Squint transforms your videos and manuals into interactive procedures, giving every new hire real-world, hands-on guidance from day one.",
			image: "/generated/image-a-diverse-group-of-frontline-workers-att.webp",
			link: {
				href: "/use-cases/operator-onboarding",
				label: "Learn more"
			}
		},
		{
			title: "Real-time task support on the floor",
			description:
				"Operators get instant help by scanning equipment or workstations with their mobile device— access step-by-step guides, videos, and AI-powered answers right in the flow of work.",
			image: "/generated/image-an-industrial-technician-is-working-dili.webp",
			link: {
				href: "/use-cases/real-time-support",
				label: "Learn more"
			}
		},
		{
			title: "Standardized maintenance and compliance tracking",
			description:
				"Digitally track inspections, repair steps, and required checks to ensure every process is completed safely and consistently— with full reports and insights for managers.",
			image: "/generated/image-a-maintenance-worker-is-actively-engaged.webp",
			link: {
				href: "/use-cases/maintenance-compliance",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction
	title="Train less. Get more done."
	subtitle="Put digital guidance in every operator's hands"
	description="Squint turns your documentation into instant, step-by-step procedures any frontline worker can use—right on the floor. Cut downtime, standardize work, and bring expertise to every shift."
	imageSrc="/generated/image-a-smiling-industrial-frontline-worker-st.webp"
	callsToAction={[
		{ href: "/demo", label: "Request a demo", variant: "primary" },
		{ href: "/contact", label: "Talk to sales", variant: "secondary" }
	]}
/>
