<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Innovation",
			description: "Constantly challenging the status quo to create better solutions."
		},
		{
			title: "Integrity",
			description: "Building trust through transparent actions and honest communication."
		},
		{
			title: "Impact",
			description: "Measuring our success by the positive change we create for our clients."
		}
	];
</script>

<SecondaryHero
  title="From static docs to smart help"
  subtitle="Squint turns your existing manuals and videos into on-the-floor guidance that improves safety, speed, and consistency"
  imageSrc="/mockups/airport-screen-1749653739297.png"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"In factories and plants, vital know-how is often buried in scattered documents or locked away in the minds of a few experts. Training new operators was slow, procedures were hard to follow, and when experienced workers left, critical knowledge walked out the door.",
		"We founded Squint to solve this—combining AI and augmented reality to turn your existing videos, spreadsheets, and PDFs into immersive, step-by-step procedures. By making that knowledge instantly accessible in the real world, any operator can get help, follow standards, and do the job right—no matter the task or their experience level.",
		"Today, Squint helps industrial teams in automotive, food and beverage, energy, and more. We’ve been named one of Fast Company’s World’s Most Innovative Companies, but our real motivation is simple: empowering every frontline worker, building a culture around connection and safety, and making it easy for operators to succeed on day one."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Meet the team."
  subtitle="People making operational excellence possible."
  stakeholders={[
    {
      name: "Devin Bhushan",
      position: "CEO & Founder",
      bio: "Devin leads Squint’s vision, bringing a background in software engineering and a passion for empowering frontline teams with intuitive tools.",
      image: "/generated/image-a-professional-headshot-of-a-south-asian.webp"
    },
    {
      name: "Dylan Conway",
      position: "Founding Customer Lead",
      bio: "Dylan works closely with our earliest industrial partners, ensuring Squint solves real operator challenges from day one.",
      image: "/generated/image-a-professional-headshot-of-a-white-male-.webp"
    },
    {
      name: "Jim Zhu",
      position: "Founding Architect",
      bio: "Jim shapes the technical foundations of Squint, focusing on robust architecture and scalable performance.",
      image: "/generated/image-a-professional-headshot-of-a-white-male-.webp"
    },
    {
      name: "Ben Weaver",
      position: "Director of Engineering",
      bio: "Ben leads engineering, ensuring Squint’s platform is secure, reliable, and delivers for every operator in the field.",
      image: "/generated/image-a-professional-headshot-of-a-white-male-.webp"
    },
    {
      name: "Hareem Mannan",
      position: "Head of Product and Design",
      bio: "Hareem blends enterprise needs with user-centered design to create seamless, effective AR procedures for customers.",
      image: "/generated/image-a-professional-headshot-of-a-white-male-.webp"
    },
    {
      name: "James Jennings",
      position: "Head of Sales",
      bio: "James partners with manufacturers to bring Squint’s solutions onto factory floors everywhere.",
      image: "/generated/image-a-professional-headshot-of-a-black-male-.webp"
    }
  ]}
/>

<StakeholderGrid
	stakeholderType="investor"
	title="Backed by the best."
	subtitle="Point Nine, TSIC and others"
	stakeholders={[
		{
			name: "Point Nine Capital",
			image: "https://cdn.brandfetch.io/pointnine.com/w/400/h/400/logo?c=1id_elLz2Bd5Ej-dWo7"
		},
		{
			name: "TSIC Ventures",
			image: "https://cdn.brandfetch.io/tiny.vc/w/400/h/400/logo?c=1a2b3c4d5e"
		},
		{
			name: "Sequoia Capital",
			image: "https://cdn.brandfetch.io/sequoiacap.com/w/400/h/400/logo"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
  title="Your operations can’t wait"
  subtitle="Standardize work. Empower every frontline team. Make excellence repeatable—right now."
  description="Tribal knowledge walks out the door every day. Inconsistent procedures slow your floor and put compliance at risk. Squint turns all your scattered documentation—videos, PDFs, spreadsheets—into consistent, easy-to-follow guidance that your teams can use immediately, directly on the job. No extra hardware, no wasted time.

The result? Faster training, fewer errors, and teams that work with confidence. Whether you're leading one facility or managing shifts globally, Squint makes it easy to scale best practices with precision.

Book a conversation or see it in action. Your floor—and your teams—deserve better than guesswork."
  callsToAction={[
    { href: '/contact', label: 'Book a demo', variant: 'primary' },
    { href: '/contact', label: 'Talk to our team', variant: 'secondary' }
  ]}
  imageSrc="/generated/image-a-diverse-industrial-team-walking-togeth.webp"
/>
