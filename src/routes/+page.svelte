<script>
	let projects = [
		{
			title: 'Exec',
			description: 'A code executor api',
			tech: ['SvelteKit', "Tailwind", 'FastAPI', 'Python'],
			link: 'https://github.com/ItzCyzmiX/Exec'
		},
		{
			title: 'Drippy', 
			description: 'An outfit recommendation system, powered by AI',
			tech: ['SvelteKit', "Tailwind", 'Groq', 'Python'],
			link: 'https://github.com/ItzCyzmiX/Drippy'
		},
        {
			title: 'CADI AYYAD English club website',
			description: 'A website for the CADI AYYAD English club',
			tech: ['SvelteKit', "Tailwind"],
			link: 'https://github.com/ItzCyzmiX/1BAC-SM2-WRITINGS'
		}
	];

	let isVisible = false;
	
	function scrollToSection(id) {
		const element = document.getElementById(id);
		element?.scrollIntoView({ behavior: 'smooth' });
	}
</script>

<svelte:head>
	<title>CyzmiX | Portfolio</title>
</svelte:head>

<main class="min-h-screen bg-gray-950 text-gray-100 relative overflow-hidden">
    <!-- Background Pattern -->
	<div class="fixed inset-0 z-0 opacity-40">
		<div class="absolute inset-0 bg-[linear-gradient(to_right,#4f4f4f2e_1px,transparent_1px),linear-gradient(to_bottom,#4f4f4f2e_1px,transparent_1px)] bg-[size:4rem_4rem] [mask-image:radial-gradient(ellipse_60%_50%_at_50%_0%,#000_70%,transparent_100%)]"></div>
	</div>

	<!-- Floating Elements -->
	<div class="fixed inset-0 z-0 overflow-hidden pointer-events-none">
		<div class="absolute -top-40 -right-40 w-80 h-80 bg-emerald-500 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob"></div>
		<div class="absolute top-0 -left-20 w-72 h-72 bg-emerald-300 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob animation-delay-2000"></div>
		<div class="absolute -bottom-32 left-20 w-96 h-96 bg-emerald-400 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob animation-delay-4000"></div>
	</div>

	<!-- Content -->
	<div class="relative z-10">
		<!-- Hero Section -->
		<section class="container mx-auto px-6 py-40">
			<div class="max-w-3xl relative ml-4">
				<div class="absolute left-[50rem] top-0 w-[35rem] h-96 bg-gradient-to-r from-emerald-300/30 to-emerald-500/10 rounded-full blur-3xl animate-pulse">
				</div>
				<div class="absolute left-[62rem] top-[10rem] h-96 w-96 bg-transparent rounded-full text-white text-2xl text-emerald-400">
					<h1 class="typewriter">Hello World!</h1>
				</div>
      
				<h1 class="text-6xl font-bold mb-6 text-white animate-fade-in">
					Hello, I'm <span class="text-emerald-400 relative inline-block hover:text-emerald-300 transition-all duration-300 hover:-translate-y-1">
						CyzmiX
						<div class="absolute -bottom-2 left-0 w-full h-1 bg-emerald-400/20 rounded-full"></div>
                        
					</span>
                    
				</h1>
				<p class="text-xl text-gray-400 mb-8 animate-fade-in animation-delay-200">A passionate developer focused on creating elegant solutions</p>
				<div class="flex gap-4 animate-fade-in animation-delay-400">
					<button 
						on:click={() => scrollToSection('projects')}
						class="px-6 py-3 bg-emerald-500 hover:bg-emerald-600 text-white rounded-lg transition-all duration-300 hover:scale-105 shadow-lg shadow-emerald-500/20 hover:shadow-emerald-500/40"
					>
						View Projects
					</button>
					<button 
						on:click={() => scrollToSection('contact')}
						class="px-6 py-3 border border-emerald-500/20 hover:border-emerald-500 text-emerald-400 rounded-lg transition-all duration-300 hover:scale-105 hover:bg-emerald-500/10"
					>
						Contact Me
					</button>
				</div>
			</div>
		</section>

		<!-- Projects Section -->
		<section id="projects" class="container mx-auto px-6 py-24">
			<h2 class="text-4xl font-bold mb-16 text-center">Featured Projects</h2>
			<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
				{#each projects as project}
					<button class="group bg-gray-900/50 backdrop-blur-sm rounded-xl p-8 transition-all duration-300 hover:scale-105 hover:bg-gray-900 border border-gray-800/50 hover:border-emerald-500/50 hover:shadow-lg hover:shadow-emerald-500/10 h-fit w-full max-w-md mx-auto text-left">
						<h3 class="text-2xl font-bold mb-4 group-hover:text-emerald-400 transition-colors">{project.title}</h3>
						<p class="text-gray-400 mb-6 line-clamp-3">{project.description}</p>
						<div class="flex flex-wrap gap-3 mb-6">
							{#each project.tech as tech}
								<span class="bg-emerald-900/30 text-emerald-400 px-4 py-1.5 rounded-full text-sm ring-1 ring-emerald-500/20 shadow-sm group-hover:ring-emerald-500/40 transition-all">{tech}</span>
							{/each}
						</div>
						<a href={project.link} target="_blank" class="inline-flex items-center text-emerald-400 hover:text-emerald-300 transition-colors">
							View Project
							<svg class="w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
							</svg>
						</a>
					</button>
				{/each}
			</div>
		</section>

		<!-- Timeline Section -->
		<section class="container mx-auto px-6 py-24">
			<h2 class="text-4xl font-bold mb-16 text-center">Experience</h2>
			<div class="relative max-w-3xl mx-auto">
				<!-- Timeline Line -->
				<div class="absolute left-1/2 transform -translate-x-1/2 w-0.5 h-full bg-gray-800"></div>

				<!-- Timeline Items -->
				<div class="space-y-12">
                    <div class="relative flex items-center justify-between group">
						<div class="w-5/12">
							<div class="bg-gray-900/50 backdrop-blur-sm p-6 rounded-xl border border-gray-800/50 hover:border-emerald-500/50 transition-all duration-300 hover:scale-105 hover:shadow-lg hover:shadow-emerald-500/10">
								<h3 class="text-xl font-bold text-emerald-400 mb-2">Inspiration</h3>
							
								<p class="text-sm text-gray-500">2016 - 2018</p>
								<p class="mt-4 text-gray-300">Started discovering the world of programming and web development.</p>
							</div>
						</div>
						<div class="absolute left-1/2 transform -translate-x-1/2 w-4 h-4 bg-emerald-400 rounded-full border-4 border-gray-900 group-hover:scale-125 transition-transform"></div>
						<div class="w-5/12"></div>
					</div>


					<!-- Item 2 -->
					<div class="relative flex items-center justify-between group">
						<div class="w-5/12"></div>
						<div class="absolute left-1/2 transform -translate-x-1/2 w-4 h-4 bg-emerald-400 rounded-full border-4 border-gray-900 group-hover:scale-125 transition-transform"></div>
						<div class="w-5/12">
							<div class="bg-gray-900/50 backdrop-blur-sm p-6 rounded-xl border border-gray-800/50 hover:border-emerald-500/50 transition-all duration-300 hover:scale-105 hover:shadow-lg hover:shadow-emerald-500/10">
								<h3 class="text-xl font-bold text-emerald-400 mb-2">Self-Teaching</h3>
						
								<p class="text-sm text-gray-500">2018 - 2024</p>
								    <p class="mt-4 text-gray-300">Built small projects, and strengthened my knowledge in programming.</p>
							</div>
						</div>
					</div>

                    <!-- Item 1 -->
                    <div class="relative flex items-center justify-between group">
                        <div class="w-5/12">
                            <div class="bg-gray-900/50 backdrop-blur-sm p-6 rounded-xl border border-gray-800/50 hover:border-emerald-500/50 transition-all duration-300 hover:scale-105 hover:shadow-lg hover:shadow-emerald-500/10">
                                <h3 class="text-xl font-bold text-emerald-400 mb-2">Freelancing</h3>
                                
                                <p class="text-sm text-gray-500">2024 - Present</p>
                                <p class="mt-4 text-gray-300">Started freelancing and working on larger scale projects.</p>
                            </div>
                        </div>
                        <div class="absolute left-1/2 transform -translate-x-1/2 w-4 h-4 bg-emerald-400 rounded-full border-4 border-gray-900 group-hover:scale-125 transition-transform"></div>
                        <div class="w-5/12"></div>
                    </div>

				</div>
			</div>
		</section>

		<!-- Skills Section -->
		<section class="container mx-auto px-6 py-24">
			<div class="text-center mb-16">
				<h2 class="text-4xl font-bold mb-6">Skills & Technologies</h2>
				<p class="text-gray-400">Technologies and tools I work with</p>
			</div>
			
			<div class="grid grid-cols-2 gap-8">
				<div class="bg-gray-900/50 backdrop-blur-sm p-6 rounded-xl border border-gray-800/50 hover:border-emerald-500/50 transition-all duration-300  hover:shadow-lg hover:shadow-emerald-500/10 text-center">
					<svg class="h-12 w-12 mx-auto mb-4 text-emerald-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
					</svg>
					<h3 class="text-lg font-bold text-emerald-400 mb-8">Frontend Development</h3>
					<div class="flex flex-wrap justify-center gap-3">
						<span class="px-3 py-1 bg-gray-800 rounded-full text-emerald-400 flex items-center gap-2 hover:bg-gray-700 transition-colors">
							<svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M1.5 0h21l-1.91 21.563L11.977 24l-8.564-2.438L1.5 0zm7.031 9.75l-.232-2.718 10.059.003.23-2.622L5.412 4.41l.698 8.01h9.126l-.326 3.426-2.91.804-2.955-.81-.188-2.11H6.248l.33 4.171L12 19.351l5.379-1.443.744-8.157H8.531z"/></svg>
							HTML
						</span>
						<span class="px-3 py-1 bg-gray-800 rounded-full text-emerald-400 flex items-center gap-2 hover:bg-gray-700 transition-colors">
							<svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M1.5 0h21l-1.91 21.563L11.977 24l-8.565-2.438L1.5 0zm17.09 4.413L5.41 4.41l.213 2.622 10.125.002-.255 2.716h-6.64l.24 2.573h6.182l-.366 3.523-2.91.804-2.956-.81-.188-2.11h-2.61l.29 3.855L12 19.288l5.373-1.53L18.59 4.414z"/></svg>
							CSS
						</span>
						<span class="px-3 py-1 bg-gray-800 rounded-full text-emerald-400 flex items-center gap-2 hover:bg-gray-700 transition-colors">
							<svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M0 0h24v24H0V0zm22.034 18.276c-.175-1.095-.888-2.015-3.003-2.873-.736-.345-1.554-.585-1.797-1.14-.091-.33-.105-.51-.046-.705.15-.646.915-.84 1.515-.66.39.12.75.42.976.9 1.034-.676 1.034-.676 1.755-1.125-.27-.42-.404-.601-.586-.78-.63-.705-1.469-1.065-2.834-1.034l-.705.089c-.676.165-1.32.525-1.71 1.005-1.14 1.291-.811 3.541.569 4.471 1.365 1.02 3.361 1.244 3.616 2.205.24 1.17-.87 1.545-1.966 1.41-.811-.18-1.26-.586-1.755-1.336l-1.83 1.051c.21.48.45.689.81 1.109 1.74 1.756 6.09 1.666 6.871-1.004.029-.09.24-.705.074-1.65l.046.067zm-8.983-7.245h-2.248c0 1.938-.009 3.864-.009 5.805 0 1.232.063 2.363-.138 2.711-.33.689-1.18.601-1.566.48-.396-.196-.597-.466-.83-.855-.063-.105-.11-.196-.127-.196l-1.825 1.125c.305.63.75 1.172 1.324 1.517.855.51 2.004.675 3.207.405.783-.226 1.458-.691 1.811-1.411.51-.93.402-2.07.397-3.346.012-2.054 0-4.109 0-6.179l.004-.056z"/></svg>
							JavaScript
						</span>
						<span class="px-3 py-1 bg-gray-800 rounded-full text-emerald-400 flex items-center gap-2 hover:bg-gray-700 transition-colors">
							<svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M23.7736 12.2262C23.7736 11.1698 22.8832 10.2794 21.8268 10.2794H14.7453C14.1547 10.2794 13.6547 9.77938 13.6547 9.18877C13.6547 8.59815 14.1547 8.09815 14.7453 8.09815H22.8379C22.9547 8.09815 23.0494 8.00346 23.0494 7.88662V2.45723C23.0494 2.34039 22.9547 2.24569 22.8379 2.24569H14.7453C11.8589 2.24569 9.51562 4.58892 9.51562 7.47538V9.18877V10.902V16.5247C9.51562 19.4111 11.8589 21.7543 14.7453 21.7543H21.8268C22.8832 21.7543 23.7736 20.8639 23.7736 19.8075V12.2262ZM6.46725 8.09815H2.21154C2.09471 8.09815 2 8.00346 2 7.88662V2.45723C2 2.34039 2.09471 2.24569 2.21154 2.24569H6.46725C7.05786 2.24569 7.55786 2.74569 7.55786 3.33631C7.55786 3.92692 7.05786 4.42692 6.46725 4.42692H4.18123V6.00346H6.46725C7.05786 6.00346 7.55786 6.50346 7.55786 7.09408C7.55786 7.68469 7.05786 8.09815 6.46725 8.09815Z"/></svg>
							Svelte
						</span>
					</div>
				</div>

				<div class="bg-gray-900/50 backdrop-blur-sm p-6 rounded-xl border border-gray-800/50 hover:border-emerald-500/50 transition-all duration-300  hover:shadow-lg hover:shadow-emerald-500/10 text-center">
					<svg class="h-12 w-12 mx-auto mb-4 text-emerald-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4" />
					</svg>
					<h3 class="text-lg font-bold text-emerald-400 mb-8">Backend Development</h3>
					<div class="flex flex-wrap justify-center gap-3">
						<span class="px-3 py-1 bg-gray-800 rounded-full text-emerald-400 flex items-center gap-2 hover:bg-gray-700 transition-colors">
							<svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M11.998,24c-0.321,0-0.641-0.084-0.922-0.247l-2.936-1.737c-0.438-0.245-0.224-0.332-0.08-0.383 c0.585-0.203,0.703-0.25,1.328-0.604c0.065-0.037,0.151-0.023,0.218,0.017l2.256,1.339c0.082,0.045,0.197,0.045,0.272,0l8.795-5.076 c0.082-0.047,0.134-0.141,0.134-0.238V6.921c0-0.099-0.053-0.192-0.137-0.242l-8.791-5.072c-0.081-0.047-0.189-0.047-0.271,0 L3.075,6.68C2.99,6.729,2.936,6.825,2.936,6.921v10.15c0,0.097,0.054,0.189,0.139,0.235l2.409,1.392 c1.307,0.654,2.108-0.116,2.108-0.89V7.787c0-0.142,0.114-0.253,0.256-0.253h1.115c0.139,0,0.255,0.112,0.255,0.253v10.021 c0,1.745-0.95,2.745-2.604,2.745c-0.508,0-0.909,0-2.026-0.551L2.28,18.675c-0.57-0.329-0.922-0.945-0.922-1.604V6.921 c0-0.659,0.353-1.275,0.922-1.603l8.795-5.082c0.557-0.315,1.296-0.315,1.848,0l8.794,5.082c0.57,0.329,0.924,0.944,0.924,1.603 v10.15c0,0.659-0.354,1.273-0.924,1.604l-8.794,5.078C12.643,23.916,12.324,24,11.998,24z M19.099,13.993 c0-1.9-1.284-2.406-3.987-2.763c-2.731-0.361-3.009-0.548-3.009-1.187c0-0.528,0.235-1.233,2.258-1.233 c1.807,0,2.473,0.389,2.747,1.607c0.024,0.115,0.129,0.199,0.247,0.199h1.141c0.071,0,0.138-0.031,0.186-0.081 c0.048-0.054,0.074-0.123,0.067-0.196c-0.177-2.098-1.571-3.076-4.388-3.076c-2.508,0-4.004,1.058-4.004,2.833 c0,1.925,1.488,2.457,3.895,2.695c2.88,0.282,3.103,0.703,3.103,1.269c0,0.983-0.789,1.402-2.642,1.402 c-2.327,0-2.839-0.584-3.011-1.742c-0.02-0.124-0.126-0.215-0.253-0.215h-1.137c-0.141,0-0.254,0.112-0.254,0.253 c0,1.482,0.806,3.248,4.655,3.248C17.501,17.007,19.099,15.91,19.099,13.993z"/></svg>
							Node.js
						</span>
						<span class="px-3 py-1 bg-gray-800 rounded-full text-emerald-400 flex items-center gap-2 hover:bg-gray-700 transition-colors">
							<svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M14.25.18l.9.2.73.26.59.3.45.32.34.34.25.34.16.33.1.3.04.26.02.2-.01.13V8.5l-.05.63-.13.55-.21.46-.26.38-.3.31-.33.25-.35.19-.35.14-.33.1-.3.07-.26.04-.21.02H8.77l-.69.05-.59.14-.5.22-.41.27-.33.32-.27.35-.2.36-.15.37-.1.35-.07.32-.04.27-.02.21v3.06H3.17l-.21-.03-.28-.07-.32-.12-.35-.18-.36-.26-.36-.36-.35-.46-.32-.59-.28-.73-.21-.88-.14-1.05-.05-1.23.06-1.22.16-1.04.24-.87.32-.71.36-.57.4-.44.42-.33.42-.24.4-.16.36-.1.32-.05.24-.01h.16l.06.01h8.16v-.83H6.18l-.01-2.75-.02-.37.05-.34.11-.31.17-.28.25-.26.31-.23.38-.2.44-.18.51-.15.58-.12.64-.1.71-.06.77-.04.84-.02 1.27.05zm-6.3 1.98l-.23.33-.08.41.08.41.23.34.33.22.41.09.41-.09.33-.22.23-.34.08-.41-.08-.41-.23-.33-.33-.22-.41-.09-.41.09zm13.09 3.95l.28.06.32.12.35.18.36.27.36.35.35.47.32.59.28.73.21.88.14 1.04.05 1.23-.06 1.23-.16 1.04-.24.86-.32.71-.36.57-.4.45-.42.33-.42.24-.4.16-.36.09-.32.05-.24.02-.16-.01h-8.22v.82h5.84l.01 2.76.02.36-.05.34-.11.31-.17.29-.25.25-.31.24-.38.2-.44.17-.51.15-.58.13-.64.09-.71.07-.77.04-.84.01-1.27-.04-1.07-.14-.9-.2-.73-.25-.59-.3-.45-.33-.34-.34-.25-.34-.16-.33-.1-.3-.04-.25-.02-.2.01-.13v-5.34l.05-.64.13-.54.21-.46.26-.38.3-.32.33-.24.35-.2.35-.14.33-.1.3-.06.26-.04.21-.02.13-.01h5.84l.69-.05.59-.14.5-.21.41-.28.33-.32.27-.35.2-.36.15-.36.1-.35.07-.32.04-.28.02-.21V6.07h2.09l.14.01zm-6.47 14.25l-.23.33-.08.41.08.41.23.33.33.23.41.08.41-.08.33-.23.23-.33.08-.41-.08-.41-.23-.33-.33-.23-.41-.08-.41.08z"/></svg>
							Python
						</span>
					</div>
				</div>
			</div>
		</section>

		<!-- Contact Section -->
        <section id="contact" class="container mx-auto px-6 py-6">
            <div class="text-center">
                <h2 class="text-4xl font-bold mb-6">Let's Connect</h2>
                <p class="text-gray-400 mb-12">Feel free to reach out for collaborations or just a friendly chat</p>
                <div class="flex justify-center gap-8">
                    <a href="https://github.com/ItzCyzmiX" target="_blank" class="text-gray-400 hover:text-emerald-400 transition-colors">
                        <span class="sr-only">GitHub</span>
                        <svg class="h-8 w-8" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                            <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd" />
                        </svg>
                    </a>
                    <a href="https://www.instagram.com/__0pium___/" target="_blank" class="text-gray-400 hover:text-emerald-400 transition-colors">
                        <span class="sr-only">Instagram</span>
                        <svg class="h-8 w-8" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                            <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/>
                        </svg>
                    </a>
                </div>
            </div>
        </section>
    
        <footer class="container mx-auto px-6 py-12">
            <p class="text-center text-gray-500">© {new Date().getFullYear()} CyzmiX. All rights reserved.</p>
        </footer>
    </main>	
    <style>
        h1.typewriter  {
          border-right: 4px solid white;
          overflow: hidden; /* Ensures the content is not revealed until the animation */
          
          white-space: nowrap; /* Keeps the content on a single line */
          /* Gives that scrolling effect as the typing happens */
          letter-spacing: .15em; /* Adjust as needed */
          animation: 
            typing 2.5s steps(40, end),
            blink-caret .75s step-end infinite;
        }
        
        /* The typing effect */
        @keyframes typing {
          from { width: 0 }
          to { width: 100%; border-right: none }
        }
        
        /* The typewriter cursor effect */
        @keyframes blink-caret {
          from, to { border-color: transparent }
          50% { border-color: white; }
        }
        </style>