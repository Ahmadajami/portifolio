<script>
	let steps = [
		{
			name: 'Smoljames Store',
			icon: 'fa-solid fa-cart-shopping',
			description:
				'Smoljames Store is a a merchanising store created with Next.js, Commerce.js & Stripe! Commerce.js is a CMS for managing project and Stripe is used for all transaction handling.'
		},
		{
			name: 'Utlimate Todos',
			icon: 'fa-solid fa-list-check',
			description:
				'Test for model robustness with customized test profiles and receive exhaustive reporting on the performance and potential vulnerabilities of your model.'
		},
		{
			name: 'Pokédex',
			icon: 'fa-solid fa-diagram-project',
			description:
				'Augment your datasets with our filters and dataset manipulations to ensure your models are trained on the highest quality datasets (coming soon).'
		}
	];

	let benefits = [
		{
			metric: '10x',
			name: 'a self taught developer',
			description:
				'I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more.'
		},
		{
			name: 'a product design & UX finatic',
			description:
				'Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences.'
		},
		{
			name: 'an excellent communicator',
			description:
				"Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team."
		}
	];
</script>

<main class="flex flex-1 flex-col p-4">
	<section id="introPage" class="grid grid-cols-1 gap-10 py-8 sm:py-14 lg:grid-cols-2">
		<div class="flex flex-col gap-6 text-center md:gap-8 lg:justify-center lg:gap-10 lg:text-left">
			<h2 class="text-4xl font-semibold sm:text-5xl md:text-6xl">
				Hi! I'm <span class="poppins text-violet-400">Ahmad</span> Alajami
				<br />FrontEnd
				<span class="poppins text-violet-400">Developer</span>
			</h2>
			<p class="text-base sm:text-lg md:text-xl">
				My <span class="text-violet-400"> favorite tech</span> includes JavaScript (SvelteKit), TailwindCSS,Flutter
				& PostgreSQL or Firebase/Firestore!
			</p>
			<button
				class="blueShadow poppins group relative mx-auto overflow-hidden rounded-full bg-white px-6 py-3 text-base text-slate-950 sm:text-lg md:text-xl lg:ml-0 lg:mr-auto"
			>
				<div
					class="absolute right-full top-0 z-0 h-full w-full bg-violet-400 opacity-20 duration-200 group-hover:translate-x-full"
				></div>
				<h4 class="z-9 relative">Get in touch &rarr;</h4>
			</button>
		</div>
		<div class="relative grid place-items-center shadow-2xl">
			<div class="vc-image-1">
				<img src={'images/profile.jpg'} alt="Profile" class="z-[2] max-h-[70vh] object-cover" />
			</div>
		</div>
	</section>
	<section class="flex flex-col gap-24 py-20 lg:py-32" id="projects">
		<div class="flex flex-col gap-2 text-center">
			<h6 class="text-large sm:text-xl md:text-2xl">A few of my creative endeavors.</h6>
			<h3 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
				Curious to <span class="poppins text-violet-400">see</span> my work?
			</h3>
		</div>
		<a
			href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
			target="_blank"
			class="mx-auto -mb-4 -mt-10 flex items-center gap-2 rounded-md border border-solid border-white px-4 py-2 duration-200 hover:border-violet-700 sm:-mb-0"
		>
			<p>Watch the video</p>
		</a>
	</section>
	<section
		id="about"
		class="relative flex flex-col gap-16 py-20 pt-10 sm:gap-20 md:gap-24 lg:py-32 lg:pt-16"
	>
		<!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
		<div
			class="relative flex flex-col gap-2 py-4 text-center before:absolute before:left-0 before:top-0 before:h-1.5 before:w-2/3 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:h-1.5 after:w-2/3 after:bg-violet-700"
		>
			<h6 class="text-large sm:text-xl md:text-2xl">Want to know more?</h6>
			<h3 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
				A bit <span class="poppins text-violet-400">about</span> me.
			</h3>
		</div>
		<p class="poppins mx-auto text-lg font-semibold sm:text-xl md:text-2xl">I am . . .</p>
		<div class="mx-auto flex w-full max-w-[800px] flex-col gap-20">
			{#each benefits as benefit, index}
				<div class="flex gap-6 sm:gap-8">
					<p class="poppins text-4xl font-semibold text-slate-500 sm:text-5xl md:text-6xl">
						0{index + 1}
					</p>
					<div class="flex flex-col gap-6 sm:gap-8">
						<h3 class="text-2xl sm:text-3xl md:text-5xl">
							{benefit.name}
						</h3>
						<p>{benefit.description}</p>
					</div>
				</div>
			{/each}
		</div>

		<div class="mx-auto -mt-12 italic opacity-50 sm:hidden">
			<p>Scroll to see more &rarr;</p>
		</div>
	</section>
</main>

<style>
	.vc-image-1 img {
		border-radius: 30% 70% 70% 30% / 30% 30% 70% 70% !important;
	}
</style>
