<script lang="ts">
	import { cn } from '$lib/utils';

	let {
		pauseOnHover = false,
		pauseOnClick = false,
		vertical = false,
		repeat = 4,
		reverse = false,
		children,
		duration = '7s'
	}: {
		pauseOnHover?: boolean;
		pauseOnClick?: boolean;
		vertical?: boolean;
		repeat?: number;
		reverse?: boolean;
		children: any;
		duration?: string;
	} = $props();

	let windowWidth = $state(0);
	let isMobile = $derived(windowWidth <= 1024);

	let className = $state<any>('');
	let isClickPaused = $state(false);

	export { className as class };

	function handleClick() {
		if (pauseOnClick && isMobile) {
			isClickPaused = !isClickPaused;
		}
	}
</script>

<svelte:window bind:innerWidth={windowWidth} />

<button
	type="button"
	class={cn(
		'group flex overflow-hidden p-2 [--gap:1rem] [gap:var(--gap)]',
		'border-none bg-transparent text-left font-normal',
		{
			'flex-row': !vertical,
			'flex-col': vertical,
			'cursor-pointer': pauseOnClick && isMobile
		},
		`[--duration:50s]`,
		className
	)}
	onclick={pauseOnClick && isMobile ? handleClick : undefined}
	aria-label={pauseOnClick && isMobile
		? isClickPaused
			? 'Resume marquee'
			: 'Pause marquee'
		: undefined}
	disabled={!(pauseOnClick && isMobile)}
>
	{#each { length: repeat } as _, i (i)}
		<div
			class={cn('flex shrink-0 justify-around [gap:var(--gap)]', 'pointer-events-none', {
				'animate-marquee flex-row': !vertical,
				'animate-marquee-vertical flex-col': vertical,
				'group-hover:[animation-play-state:paused]': pauseOnHover && !isClickPaused,
				'[animation-play-state:paused]': isClickPaused,
				'[animation-direction:reverse]': reverse
			})}
		>
			{@render children()}
		</div>
	{/each}
</button>
