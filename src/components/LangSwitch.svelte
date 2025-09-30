<script lang="ts">
	import { onMount } from "svelte";
    import Icon from "@iconify/svelte";
    import { fly, fade } from "svelte/transition";

	let open = false;

	const LANGUAGES = [
		{ label: "English", url: "https://chemmasterynahida.github.io" },
		{ label: "Français", url: "https://chemmasterynahida.github.io/fr/"},
		{ label: "简体中文", url: "https://chemmasterynahida.github.io/zhcn/" },
        { label: "繁體中文", url: "https://chemmasterynahida.github.io/zhtw/" },
        { label: "日本語", url: "https://chemmasterynahida.github.io/ja/" },
		{ label: "한국어", url: "https://chemmasterynahida.github.io/ko/" }
	];

	function toggleMenu() {
		open = !open;
	}

	// close dropdown on outside click
	onMount(() => {
		function handleClick(e: MouseEvent) {
			if (!(e.target as HTMLElement).closest("#lang-switch")) {
				open = false;
			}
		}
		document.addEventListener("click", handleClick);
		return () => document.removeEventListener("click", handleClick);
	});
</script>

<style>
.dropdown {
	position: absolute;
	top: 100%;
	right: 0;
	background: var(--card-bg);
	border-radius: 0.5rem;
	padding: 0.5rem 0;
	box-shadow: 0 4px 12px rgba(0,0,0,0.15);
	z-index: 50;
}
.dropdown a {
	display: block;
	padding: 0.5rem 1rem;
	white-space: nowrap;
	cursor: pointer;
	transition: background 0.2s ease;
}
.dropdown a:hover {
	background: var(--hover-bg, #eee);
}
</style>

<div id="lang-switch" class="relative">
	<button
		aria-label="Language Switch"
		class="btn-plain scale-animation rounded-lg h-11 w-11 active:scale-90"
		on:click={toggleMenu}
	>
		<Icon icon="iconoir:translate" class="text-[1.25rem]"></Icon>
	</button>

	{#if open}
		<div
			class="dropdown"
			in:fly={{ y: -5, duration: 150 }}
			out:fade={{ duration: 100 }}
		>
			{#each LANGUAGES as lang}
				<a href={lang.url} target="_blank" rel="noopener noreferrer">
					{lang.label}
				</a>
			{/each}
		</div>
	{/if}
</div>
