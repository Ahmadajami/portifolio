<script lang="ts">
	import Header from '$lib/Header.svelte';
	import Uparrow from '$lib/Icon/Uparrow.svelte';
	import '../app.css';
	let { children } = $props();
	let innerHeight = $state(0);
	let innerWidth = $state(0);
	let y = $state() as number;
	function goTop() {
		document.body.scrollIntoView();
	}
</script>

<div class="max-w[1400px] min-h relative mx-auto flex w-full flex-col">
	<div
		class={'fixed bottom-0 z-[10] flex w-full p-10 duration-200 ' +
			(y > 0 ? ' opacity-full pointer-events-auto' : ' pointer-events-none opacity-0')}
	>
		<button
			onclick={goTop}
			class="ml-auto grid aspect-square cursor-pointer place-items-center rounded-full bg-slate-900 px-3 text-violet-400 hover:bg-slate-800 sm:px-4"
		>
			<Uparrow />
		</button>
	</div>
	<Header {y} />
	{@render children()}
</div>
<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
