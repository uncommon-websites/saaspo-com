<script lang="ts">
	import { onMount } from 'svelte';
</script>

<div class="max-w-[1400px] mx-auto px-6 pt-12 pb-24">
	<!-- Navbar -->
	<nav class="flex items-center justify-between py-4 mb-20">
		<div class="flex items-center gap-2">
			<div class="w-8 h-8 bg-[#00f2a9] rounded-md flex items-center justify-center">
				<svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
					<path d="M2 17L12 22L22 17" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
					<path d="M2 12L12 17L22 12" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
				</svg>
			</div>
			<span class="text-xl font-bold tracking-tight">saaspo</span>
		</div>

		<div class="hidden md:flex items-center gap-8 text-sm font-medium text-gray-400">
			<a href="#" class="flex flex-col items-center hover:text-white transition-colors">
				<span class="text-[#00f2a9] text-[10px] mb-0.5">2900</span>
				<span class="text-white">Pages</span>
			</a>
			<a href="#" class="flex flex-col items-center hover:text-white transition-colors">
				<span class="text-[#00f2a9] text-[10px] mb-0.5">709</span>
				<span>Sections</span>
			</a>
			<a href="#" class="flex flex-col items-center hover:text-white transition-colors">
				<span class="text-[#00f2a9] text-[10px] mb-0.5">355</span>
				<span>OG images</span>
			</a>
			<a href="#" class="flex flex-col items-center hover:text-white transition-colors">
				<span class="text-[#00f2a9] text-[10px] mb-0.5">27</span>
				<span>Templates</span>
			</a>
			<button class="flex items-center gap-1 hover:text-white transition-colors mt-3">
				More
				<svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg>
			</button>
		</div>

		<button class="bg-[#00f2a9] text-black px-4 py-2 rounded-md font-medium text-sm flex items-center gap-2 hover:bg-[#00d695] transition-colors">
			Random
			<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"/><polyline points="3.27 6.96 12 12.01 20.73 6.96"/><line x1="12" y1="22.08" x2="12" y2="12"/></svg>
		</button>
	</nav>

	<!-- Hero Section -->
	<div class="flex flex-col lg:flex-row justify-between items-start gap-12 mb-16">
		<div class="max-w-2xl">
			<h1 class="text-5xl md:text-6xl font-bold leading-[1.1] mb-6 tracking-tight">
				The best SaaS web<br />design inspiration
			</h1>
			<p class="text-gray-400 text-lg mb-8 max-w-xl leading-relaxed">
				A curated collection of the best SaaS landing pages on the web. Quickly find the design inspiration you're looking for with our <span class="text-[#00f2a9]">filters</span>.
			</p>
			
			<div class="flex items-center gap-3">
				<span class="text-sm text-gray-500">Sponsored by:</span>
				<div class="flex gap-2">
					<div class="w-8 h-8 bg-[#2C2C2C] rounded-md flex items-center justify-center"><img src="https://upload.wikimedia.org/wikipedia/commons/3/33/Figma-logo.svg" alt="Figma" class="w-5 h-5" /></div>
					<div class="w-8 h-8 bg-[#2C2C2C] rounded-md flex items-center justify-center"><img src="https://upload.wikimedia.org/wikipedia/commons/a/a7/React-icon.svg" alt="React" class="w-5 h-5" /></div>
					<div class="w-8 h-8 bg-[#2C2C2C] rounded-md flex items-center justify-center"><img src="https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg" alt="Tailwind" class="w-5 h-5" /></div>
					<div class="w-8 h-8 bg-[#2C2C2C] rounded-md flex items-center justify-center"><img src="https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg" alt="AWS" class="w-5 h-5" /></div>
					<button class="w-8 h-8 bg-[#1A1A1A] border border-gray-800 rounded-md flex items-center justify-center text-gray-400 hover:text-white transition-colors">
						<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="M12 5v14"/></svg>
					</button>
				</div>
			</div>
		</div>

		<div class="w-full lg:w-[400px] bg-[#1A1A1A] border border-gray-800 rounded-2xl p-8 relative overflow-hidden">
			<div class="absolute top-0 right-0 w-32 h-32 bg-[#00f2a9]/10 blur-[50px] rounded-full"></div>
			<h2 class="text-2xl font-bold mb-4 leading-tight">Get the 7 best<br />SaaS<br />designs in your<br />inbox<br />each week.</h2>
			<p class="text-gray-400 text-sm mb-6">Join 2,258+ other designers.</p>
			<form class="flex gap-2" on:submit|preventDefault>
				<input type="email" placeholder="Enter your email" class="flex-1 bg-white text-black px-4 py-3 rounded-md text-sm outline-none placeholder:text-gray-500" />
				<button type="submit" class="bg-[#00f2a9] text-black px-6 py-3 rounded-md font-medium text-sm hover:bg-[#00d695] transition-colors whitespace-nowrap">
					Subscribe
				</button>
			</form>
		</div>
	</div>

	<!-- Filters -->
	<div class="mb-8">
		<div class="flex gap-4 mb-6">
			<button class="bg-white text-black px-4 py-1.5 rounded-full text-sm font-medium">Pages</button>
			<button class="text-gray-400 hover:text-white px-4 py-1.5 rounded-full text-sm font-medium transition-colors">Sections</button>
			<button class="text-gray-400 hover:text-white px-4 py-1.5 rounded-full text-sm font-medium transition-colors">OG images</button>
		</div>

		<div class="flex flex-wrap gap-3">
			{#each ['Page types', 'Industry', 'Style', 'Assets', 'Stack'] as filter}
				<button class="bg-[#1A1A1A] border border-gray-800 text-gray-300 px-4 py-2.5 rounded-md text-sm flex items-center gap-2 hover:bg-[#222] transition-colors flex-1 min-w-[150px] justify-between">
					{filter}
					<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg>
				</button>
			{/each}
		</div>
	</div>

	<!-- Grid -->
	<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-16">
		<!-- Card 1 -->
		<div class="bg-[#1A1A1A] border border-gray-800 rounded-xl overflow-hidden group">
			<div class="flex items-center justify-between px-4 py-3 border-b border-gray-800">
				<div class="flex gap-1.5">
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
				</div>
				<span class="text-xs text-gray-400 font-medium">conway.ai/</span>
				<button class="text-gray-500 hover:text-white transition-colors">
					<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
				</button>
			</div>
			<div class="aspect-[4/3] bg-gray-900 relative overflow-hidden">
				<img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&fit=crop&q=80&w=800" alt="Conway AI" class="w-full h-full object-cover object-top opacity-80 group-hover:opacity-100 transition-opacity duration-300" />
			</div>
		</div>

		<!-- Card 2 -->
		<div class="bg-[#1A1A1A] border border-gray-800 rounded-xl overflow-hidden group">
			<div class="flex items-center justify-between px-4 py-3 border-b border-gray-800">
				<div class="flex gap-1.5">
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
				</div>
				<span class="text-xs text-gray-400 font-medium">quiver.ai/</span>
				<button class="text-gray-500 hover:text-white transition-colors">
					<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
				</button>
			</div>
			<div class="aspect-[4/3] bg-gray-900 relative overflow-hidden">
				<img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&q=80&w=800" alt="Quiver AI" class="w-full h-full object-cover object-top opacity-80 group-hover:opacity-100 transition-opacity duration-300" />
			</div>
		</div>

		<!-- Card 3 -->
		<div class="bg-[#1A1A1A] border border-gray-800 rounded-xl overflow-hidden group relative">
			<div class="absolute -top-3 left-1/2 -translate-x-1/2 bg-[#00f2a9] text-black text-[10px] font-bold px-2 py-0.5 rounded-sm z-10">Sponsored</div>
			<div class="flex items-center justify-between px-4 py-3 border-b border-gray-800">
				<div class="flex gap-1.5">
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
				</div>
				<span class="text-xs text-gray-400 font-medium">framer.com/</span>
				<button class="text-gray-500 hover:text-white transition-colors">
					<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
				</button>
			</div>
			<div class="aspect-[4/3] bg-gray-900 relative overflow-hidden">
				<img src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?auto=format&fit=crop&q=80&w=800" alt="Framer" class="w-full h-full object-cover object-top opacity-80 group-hover:opacity-100 transition-opacity duration-300" />
			</div>
		</div>
		
		<!-- Add more cards to fill the grid -->
		{#each Array(6) as _, i}
		<div class="bg-[#1A1A1A] border border-gray-800 rounded-xl overflow-hidden group">
			<div class="flex items-center justify-between px-4 py-3 border-b border-gray-800">
				<div class="flex gap-1.5">
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
					<div class="w-2.5 h-2.5 rounded-full bg-gray-700"></div>
				</div>
				<span class="text-xs text-gray-400 font-medium">example.com/</span>
				<button class="text-gray-500 hover:text-white transition-colors">
					<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
				</button>
			</div>
			<div class="aspect-[4/3] bg-gray-900 relative overflow-hidden">
				<img src={`https://images.unsplash.com/photo-${1500000000000 + i}?auto=format&fit=crop&q=80&w=800`} alt="Example" class="w-full h-full object-cover object-top opacity-80 group-hover:opacity-100 transition-opacity duration-300" />
			</div>
		</div>
		{/each}
	</div>

	<div class="flex justify-center mb-32">
		<button class="bg-white text-black px-6 py-2.5 rounded-md font-medium text-sm hover:bg-gray-200 transition-colors">
			Load more
		</button>
	</div>

	<!-- FAQ Section -->
	<div class="max-w-4xl mx-auto flex flex-col md:flex-row gap-12 items-start mb-32">
		<h2 class="text-4xl font-bold leading-tight md:w-1/3">Frequently Asked<br />Questions</h2>
		<div class="md:w-2/3 flex flex-col gap-4 w-full">
			<button class="flex items-center justify-between py-4 border-b border-gray-800 text-left hover:text-[#00f2a9] transition-colors w-full">
				<span class="font-medium">What is a SaaS website?</span>
				<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg>
			</button>
			<button class="flex items-center justify-between py-4 border-b border-gray-800 text-left hover:text-[#00f2a9] transition-colors w-full">
				<span class="font-medium">Do you only list SaaS websites?</span>
				<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg>
			</button>
		</div>
	</div>
</div>

