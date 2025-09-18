<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import { Menu, X } from 'lucide-svelte';

	let { children } = $props();
	let mobileMenuOpen = $state(false);

	const navItems = [
		{ href: '#about', label: 'About' },
		{ href: '#education', label: 'Education' },
		{ href: '#experience', label: 'Experience' },
		{ href: '#projects', label: 'Projects' },
		{ href: '#skills', label: 'Skills' },
		{ href: '#contact', label: 'Contact' }
	];

	function scrollToSection(href: string) {
		const element = document.querySelector(href);
		if (element) {
			element.scrollIntoView({ behavior: 'smooth' });
			mobileMenuOpen = false;
		}
	}
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<div class="min-h-screen bg-gradient-to-br from-slate-50 to-blue-50">
	<!-- Navigation -->
	<nav class="fixed top-0 z-50 w-full bg-white/80 backdrop-blur-md border-b border-gray-200">
		<div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
			<div class="flex h-16 items-center justify-between">
				<div class="flex-shrink-0">
					<h1 class="text-xl font-bold text-gray-900">Jonah Bray</h1>
				</div>

				<!-- Desktop Navigation -->
				<div class="hidden md:block">
					<div class="ml-10 flex items-baseline space-x-4">
						{#each navItems as item}
							<button
								onclick={() => scrollToSection(item.href)}
								class="px-3 py-2 text-sm font-medium text-gray-700 hover:text-blue-600 transition-colors duration-200"
							>
								{item.label}
							</button>
						{/each}
					</div>
				</div>

				<!-- Mobile menu button -->
				<div class="md:hidden">
					<button
						onclick={() => (mobileMenuOpen = !mobileMenuOpen)}
						class="inline-flex items-center justify-center p-2 rounded-md text-gray-700 hover:text-blue-600 hover:bg-gray-100 transition-colors duration-200"
					>
						{#if mobileMenuOpen}
							<X size={24} />
						{:else}
							<Menu size={24} />
						{/if}
					</button>
				</div>
			</div>
		</div>

		<!-- Mobile Navigation Menu -->
		{#if mobileMenuOpen}
			<div class="md:hidden bg-white border-t border-gray-200">
				<div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
					{#each navItems as item}
						<button
							onclick={() => scrollToSection(item.href)}
							class="block w-full text-left px-3 py-2 text-base font-medium text-gray-700 hover:text-blue-600 hover:bg-gray-50 transition-colors duration-200"
						>
							{item.label}
						</button>
					{/each}
				</div>
			</div>
		{/if}
	</nav>

	<!-- Main Content -->
	<main class="pt-16">
		{@render children?.()}
	</main>
</div>
