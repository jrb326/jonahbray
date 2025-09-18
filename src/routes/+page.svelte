<script lang="ts">
	import { onMount } from 'svelte';
	import { 
		ChevronDown, 
		MapPin, 
		Calendar, 
		Mail, 
		Github, 
		Linkedin, 
		ExternalLink,
		GraduationCap,
		Briefcase,
		Code,
		Award,
		Users,
		Database,
		Server,
		Globe
	} from 'lucide-svelte';

	let mounted = $state(false);

	onMount(() => {
		mounted = true;
	});

	const skills = {
		languages: ['R', 'Java', 'SQL', 'Rust', 'C', 'Dart', 'JavaScript', 'Python'],
		technologies: ['Docker', 'AWS', 'Azure', 'React', 'Node.js', 'MongoDB', 'PostgreSQL', 'Next.js', 'Flask', '.NET'],
		tools: ['Git', 'Nginx', 'Grafana', 'Proxmox', 'PXE', 'Ubuntu', 'Jira']
	};

	const experiences = [
		{
			title: 'Junior System Administrator',
			company: 'Lehigh University',
			period: 'August 2025 - Current',
			description: 'Within the CSE (Computer Science Engineering) department, worked to help maintain and create physical systems and software of the university, by using with networking systems, proxmox, grafana, PXE, ubuntu os, etc..',
			icon: Server
		},
		{
			title: 'Backend Developer',
			company: 'Epilogue Systems Inc',
			period: 'August 2025 - Current',
			description: 'Worked as a backend .NET developer, working on their core offerings and API\'s as directed through Jira tickets.',
			icon: Code
		},
		{
			title: 'Full Stack Developer Intern',
			company: 'Bulkitrade',
			period: 'Jan 2025 - July 2025',
			description: 'Used the MERN stack (mongo, express, react, node) and Postgres alongside Azure Cloud and AWS to maintain Bulkitrade\'s website and implement features across the stack.',
			icon: Globe
		}
	];

	const projects = [
		{
			title: 'React AI Modules - Senior Capstone Project',
			company: 'Merck',
			description: 'Work to develop an internal Agent & Frontend framework that can independently investigate user questions about business information, retrieve information from databases, and provide automated analysis using AWS, Next.js, and Flask.',
			technologies: ['AWS', 'Next.js', 'Flask', 'React', 'AI/ML']
		},
		{
			title: 'Cybersecurity War Games',
			description: 'Led a team in simulating realistic cyberattack scenarios using Nginx WAF, Logging stacks, Honeypots, and red team tools',
			technologies: ['Nginx', 'Security', 'Linux', 'Networking']
		},
		{
			title: 'Generative AI Texture Creator',
			description: 'Used LoRA training on Stable Diffusion Large v3 to generate pixel art assets with a desired format and style',
			technologies: ['Python', 'Stable Diffusion', 'LoRA', 'AI/ML']
		},
		{
			title: 'TheModSquad',
			description: 'Implemented an integration between Twitch and Discord that tracks user punishments in channels, as well as messages. Currently tracking 1M+ users and 10M+ messages.',
			technologies: ['Node.js', 'Discord API', 'Twitch API', 'Database']
		}
	];

	const courses = [
		'Data Science',
		'Generative AI',
		'Networking Security',
		'Embedded Programming',
		'Theory of Computation',
		'Data Structures & Algorithms',
		'Software Engineering',
		'Database Systems'
	];
</script>

<svelte:head>
	<title>Jonah Bray - Software Developer</title>
	<meta name="description" content="Computer Science student at Lehigh University specializing in full-stack development, AI, and system administration." />
</svelte:head>

<!-- Hero Section -->
<section id="about" class="relative min-h-screen flex items-center justify-center px-4 sm:px-6 lg:px-8">
	<div class="max-w-4xl mx-auto text-center">
		<div class="animate-fade-in-up opacity-0 translate-y-8 transition-all duration-1000" class:opacity-100={mounted} class:translate-y-0={mounted}>
			<h1 class="text-4xl sm:text-6xl lg:text-7xl font-bold text-gray-900 mb-6">
				Hi, I'm <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-purple-600">Jonah Bray</span>
			</h1>
			<p class="text-xl sm:text-2xl text-gray-600 mb-8 max-w-3xl mx-auto">
				Computer Science student at Lehigh University passionate about building innovative software solutions and exploring the intersection of AI and technology.
			</p>
			<div class="flex flex-col sm:flex-row gap-4 justify-center items-center mb-12">
				<div class="flex items-center text-gray-600">
					<GraduationCap class="mr-2" size={20} />
					<span>B.S Computer Science, Lehigh University</span>
				</div>
				<div class="flex items-center text-gray-600">
					<Calendar class="mr-2" size={20} />
					<span>Graduating May 2026</span>
				</div>
			</div>
			<div class="flex gap-4 justify-center">
				<a href="#contact" class="bg-blue-600 hover:bg-blue-700 text-white px-8 py-3 rounded-lg font-medium transition-colors duration-200">
					Get In Touch
				</a>
				<a href="#projects" class="border border-gray-300 hover:border-gray-400 text-gray-700 px-8 py-3 rounded-lg font-medium transition-colors duration-200">
					View Projects
				</a>
			</div>
		</div>
	</div>
	<div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
		<ChevronDown size={32} class="text-gray-400" />
	</div>
</section>

<!-- Education Section -->
<section id="education" class="py-20 px-4 sm:px-6 lg:px-8">
	<div class="max-w-6xl mx-auto">
		<div class="text-center mb-16">
			<h2 class="text-3xl sm:text-4xl font-bold text-gray-900 mb-4">Education</h2>
			<p class="text-xl text-gray-600">Academic journey and coursework</p>
		</div>

		<div class="bg-white rounded-2xl shadow-xl p-8 mb-8">
			<div class="flex flex-col lg:flex-row items-start lg:items-center gap-6">
				<div class="flex-shrink-0">
					<div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center">
						<GraduationCap size={32} class="text-blue-600" />
					</div>
				</div>
				<div class="flex-grow">
					<h3 class="text-2xl font-bold text-gray-900 mb-2">Bachelor of Science in Computer Science</h3>
					<p class="text-lg text-blue-600 font-medium mb-2">Lehigh University</p>
					<p class="text-gray-600 mb-4">Expected Graduation: May 2026</p>
				</div>
			</div>
		</div>

		<div class="bg-white rounded-2xl shadow-xl p-8">
			<h4 class="text-xl font-bold text-gray-900 mb-6">Relevant Coursework</h4>
			<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
				{#each courses as course}
					<div class="bg-gray-50 rounded-lg p-4 hover:bg-gray-100 transition-colors duration-200">
						<span class="text-gray-800 font-medium">{course}</span>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>

<!-- Experience Section -->
<section id="experience" class="py-20 px-4 sm:px-6 lg:px-8 bg-gray-50">
	<div class="max-w-6xl mx-auto">
		<div class="text-center mb-16">
			<h2 class="text-3xl sm:text-4xl font-bold text-gray-900 mb-4">Work Experience</h2>
			<p class="text-xl text-gray-600">Professional journey and achievements</p>
		</div>

		<div class="space-y-8">
			{#each experiences as experience, index}
				<div class="bg-white rounded-2xl shadow-xl p-8 hover:shadow-2xl transition-shadow duration-300">
					<div class="flex flex-col lg:flex-row items-start gap-6">
						<div class="flex-shrink-0">
							<div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center">
								<svelte:component this={experience.icon} size={32} class="text-blue-600" />
							</div>
						</div>
						<div class="flex-grow">
							<div class="flex flex-col lg:flex-row lg:items-center lg:justify-between mb-4">
								<div>
									<h3 class="text-2xl font-bold text-gray-900 mb-1">{experience.title}</h3>
									<p class="text-lg text-blue-600 font-medium">{experience.company}</p>
								</div>
								<div class="flex items-center text-gray-600 mt-2 lg:mt-0">
									<Calendar class="mr-2" size={16} />
									<span class="text-sm">{experience.period}</span>
								</div>
							</div>
							<p class="text-gray-700 leading-relaxed">{experience.description}</p>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- Projects Section -->
<section id="projects" class="py-20 px-4 sm:px-6 lg:px-8">
	<div class="max-w-6xl mx-auto">
		<div class="text-center mb-16">
			<h2 class="text-3xl sm:text-4xl font-bold text-gray-900 mb-4">Featured Projects</h2>
			<p class="text-xl text-gray-600">Showcasing my technical skills and creativity</p>
		</div>

		<div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
			{#each projects as project}
				<div class="bg-white rounded-2xl shadow-xl p-8 hover:shadow-2xl transition-all duration-300 hover:-translate-y-1">
					<div class="mb-6">
						<h3 class="text-xl font-bold text-gray-900 mb-2">{project.title}</h3>
						{#if project.company}
							<p class="text-blue-600 font-medium mb-3">{project.company}</p>
						{/if}
						<p class="text-gray-700 leading-relaxed">{project.description}</p>
					</div>
					<div class="flex flex-wrap gap-2">
						{#each project.technologies as tech}
							<span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm font-medium">
								{tech}
							</span>
						{/each}
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- Skills Section -->
<section id="skills" class="py-20 px-4 sm:px-6 lg:px-8 bg-gray-50">
	<div class="max-w-6xl mx-auto">
		<div class="text-center mb-16">
			<h2 class="text-3xl sm:text-4xl font-bold text-gray-900 mb-4">Skills & Technologies</h2>
			<p class="text-xl text-gray-600">Technical expertise and certifications</p>
		</div>

		<div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-12">
			<div class="bg-white rounded-2xl shadow-xl p-8">
				<div class="flex items-center mb-6">
					<Code size={32} class="text-blue-600 mr-3" />
					<h3 class="text-xl font-bold text-gray-900">Programming Languages</h3>
				</div>
				<div class="flex flex-wrap gap-2">
					{#each skills.languages as language}
						<span class="bg-blue-100 text-blue-800 px-3 py-2 rounded-lg text-sm font-medium">
							{language}
						</span>
					{/each}
				</div>
			</div>

			<div class="bg-white rounded-2xl shadow-xl p-8">
				<div class="flex items-center mb-6">
					<Database size={32} class="text-green-600 mr-3" />
					<h3 class="text-xl font-bold text-gray-900">Technologies & Frameworks</h3>
				</div>
				<div class="flex flex-wrap gap-2">
					{#each skills.technologies as tech}
						<span class="bg-green-100 text-green-800 px-3 py-2 rounded-lg text-sm font-medium">
							{tech}
						</span>
					{/each}
				</div>
			</div>

			<div class="bg-white rounded-2xl shadow-xl p-8">
				<div class="flex items-center mb-6">
					<Server size={32} class="text-purple-600 mr-3" />
					<h3 class="text-xl font-bold text-gray-900">Tools & Platforms</h3>
				</div>
				<div class="flex flex-wrap gap-2">
					{#each skills.tools as tool}
						<span class="bg-purple-100 text-purple-800 px-3 py-2 rounded-lg text-sm font-medium">
							{tool}
						</span>
					{/each}
				</div>
			</div>
		</div>

		<!-- Certifications -->
		<div class="bg-white rounded-2xl shadow-xl p-8">
			<div class="flex items-center mb-6">
				<Award size={32} class="text-yellow-600 mr-3" />
				<h3 class="text-xl font-bold text-gray-900">Certifications</h3>
			</div>
			<div class="bg-yellow-50 border border-yellow-200 rounded-lg p-4">
				<span class="text-yellow-800 font-medium">Microsoft Certified Java Programmer SE 8</span>
			</div>
		</div>
	</div>
</section>

<!-- Contact Section -->
<section id="contact" class="py-20 px-4 sm:px-6 lg:px-8">
	<div class="max-w-4xl mx-auto text-center">
		<div class="mb-16">
			<h2 class="text-3xl sm:text-4xl font-bold text-gray-900 mb-4">Let's Connect</h2>
			<p class="text-xl text-gray-600">I'm always open to discussing new opportunities and interesting projects</p>
		</div>

		<div class="bg-white rounded-2xl shadow-xl p-8 mb-8">
			<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
				<a href="mailto:jonah@example.com" class="flex flex-col items-center p-6 hover:bg-gray-50 rounded-lg transition-colors duration-200">
					<Mail size={32} class="text-blue-600 mb-3" />
					<span class="text-gray-900 font-medium">Email</span>
					<span class="text-gray-600 text-sm">Get in touch</span>
				</a>
				<a href="https://github.com" target="_blank" rel="noopener noreferrer" class="flex flex-col items-center p-6 hover:bg-gray-50 rounded-lg transition-colors duration-200">
					<Github size={32} class="text-gray-900 mb-3" />
					<span class="text-gray-900 font-medium">GitHub</span>
					<span class="text-gray-600 text-sm">View my code</span>
				</a>
				<a href="https://linkedin.com" target="_blank" rel="noopener noreferrer" class="flex flex-col items-center p-6 hover:bg-gray-50 rounded-lg transition-colors duration-200">
					<Linkedin size={32} class="text-blue-600 mb-3" />
					<span class="text-gray-900 font-medium">LinkedIn</span>
					<span class="text-gray-600 text-sm">Professional network</span>
				</a>
			</div>
		</div>

		<p class="text-gray-600">
			Currently seeking <strong>full-time opportunities</strong> starting Summer 2026. 
			Let's build something amazing together!
		</p>
	</div>
</section>

<!-- Footer -->
<footer class="bg-gray-900 text-white py-12 px-4 sm:px-6 lg:px-8">
	<div class="max-w-6xl mx-auto text-center">
		<p class="text-gray-400 mb-4">© 2025 Jonah Bray. Built with SvelteKit and TailwindCSS.</p>
		<p class="text-gray-500 text-sm">Designed with ❤️ for showcasing my journey in Computer Science</p>
	</div>
</footer>

<style>
	.animate-fade-in-up {
		animation: fadeInUp 1s ease-out forwards;
	}

	@keyframes fadeInUp {
		from {
			opacity: 0;
			transform: translateY(2rem);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	html {
		scroll-behavior: smooth;
	}
</style>
