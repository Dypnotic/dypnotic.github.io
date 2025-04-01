<script lang="ts">
	import type { LayoutProps } from "./$types";

	let { children }: LayoutProps = $props();
</script>

<svelte:head>
	<link href="/media/images/dypnotic-logo.svg" rel="icon" />
	<link rel="preconnect" href="https://fonts.bunny.net" />
	<style>
	</style>
	<link rel="stylesheet" href="/style.css" />
</svelte:head>
<nav class="menu">
	<a href="/"
		><img
			width="50"
			height="50"
			src="/media/images/dypnotic-logo.svg"
			alt="The Dypnotic Logo. A fat cross with a short arrow on the bottom pointing up. It is an abstraction of a palm tree."
		/></a
	>
</nav>

{@render children()}

<style>
	/* latin regular*/
	@font-face {
		font-family: "JetBrains Mono";
		font-style: normal;
		font-weight: 400;
		font-stretch: 100%;
		font-display: swap;
		src:
			url(https://fonts.bunny.net/jetbrains-mono/files/jetbrains-mono-latin-400-normal.woff2)
				format("woff2"),
			url(https://fonts.bunny.net/jetbrains-mono/files/jetbrains-mono-latin-400-normal.woff)
				format("woff");
		unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA,
			U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+2074, U+20AC, U+2122,
			U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
	}

	/* latin bold*/
	@font-face {
		font-family: "JetBrains Mono";
		font-style: normal;
		font-weight: 700;
		font-stretch: 100%;
		font-display: swap;
		src:
			url(https://fonts.bunny.net/jetbrains-mono/files/jetbrains-mono-latin-700-normal.woff2)
				format("woff2"),
			url(https://fonts.bunny.net/jetbrains-mono/files/jetbrains-mono-latin-700-normal.woff)
				format("woff");
		unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA,
			U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+2074, U+20AC, U+2122,
			U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
	}

	/* latin italic*/
	@font-face {
		font-family: "JetBrains Mono";
		font-style: italic;
		font-weight: 400;
		font-stretch: 100%;
		font-display: swap;
		src:
			url(https://fonts.bunny.net/jetbrains-mono/files/jetbrains-mono-latin-400-italic.woff2)
				format("woff2"),
			url(https://fonts.bunny.net/jetbrains-mono/files/jetbrains-mono-latin-400-italic.woff)
				format("woff");
		unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA,
			U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+2074, U+20AC, U+2122,
			U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
	}

	:global(:root) {
		/* Colors */
		--bg: #f1f1f1;
		--fg: #112;
		--prime: #c00;
		--subtext: #667;

		/* Sizes */
		--font-size-s: 0.75rem;
		--font-size-m: 0.8125rem;
		--font-size-l: 1rem;
		--font-size-xl: 1.125rem;
		--font-size-2xl: 1.3125rem;
		--font-size-3xl: 1.5rem;
		--font-size-4xl: 2.652rem;
		--font-size-5xl: 4rem;

		--max-text-width: 70ch;
	}

	:global(:html) {
		height: 100%;
		width: 100%;
	}

	:global([lang="en"]) {
		font:
			var(--font-size-m) "JetBrains Mono",
			monospace;
	}

	:global([lang="ja"]) {
		font-family: Arial, Helvetica, sans-serif;
	}
	:global(body) {
		margin: 0;
		background: var(--bg);
		padding: 20px;
		color: var(--fg);
	}

	:global(::selection) {
		color: #fff;
		background: var(--prime);
	}

	:global(h1, h2) {
		padding: 16px 0;
		margin: 0;
		letter-spacing: 2px;
		display: flex;
		flex-direction: column;
	}

	:global(strong, em, cite) {
		color: #00c;
	}

	:global(ruby) {
		color: var(--prime);
	}

	:global(rt) {
		color: var(--subtext);
		font-size: 0.7em;
	}

	:global(.translation) {
		font-size: 0.6em;
		text-shadow: none;
		letter-spacing: 0;
		margin-bottom: 4px;
		color: var(--subtext);
	}

	:global(figure) {
		margin-inline: 16px;

		@media (min-width: 500px) {
			margin-inline: 40px;
		}
	}

	:global(figcaption) {
		text-align: right;
	}
</style>
