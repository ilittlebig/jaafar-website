<script lang="ts">
	import { page } from "$app/stores";
	import { cn } from "$lib/utils";
	import { Button } from "$lib/components/ui/button";

	const pages = [
		{ href: "/", label: "Home" },
		{ href: "/features", label: "Features" },
		{ href: "/pricing", label: "Pricing" },
		{ href: "/about", label: "About" },
	];
</script>

<div class="flex items-center bg-background border-b h-16">
	<div class="flex justify-between items-center w-full max-w-6xl mx-auto">
		<div class="flex gap-x-8 items-center">
			<a href="/" class="h-fit">
				<img src="jaafar.svg" alt="Logo" class="w-14" />
			</a>
			<div class="flex gap-x-8">
				{#each pages as pageData}
					<a href={pageData.href} class={cn("text-sm font-medium", $page.url.pathname !== pageData.href && "text-muted-foreground")}>
						{pageData.label}
					</a>
				{/each}
			</div>
		</div>
		<div class="flex gap-x-4">
			<Button size="sm" variant="ghost">Sign in</Button>
			<Button size="sm">Get Started</Button>
		</div>
	</div>
</div>
