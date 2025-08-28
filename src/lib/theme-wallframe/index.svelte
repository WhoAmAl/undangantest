<script>
    import Opening from '../sections/section-opening-wallframe.svelte';
    import Quote from '../sections/section-quote-wallframe.svelte';
    import Bride from '../sections/section-bride-wallframe.svelte';
    import Groom from '../sections/section-groom-wallframe.svelte';
    import Story from '../sections/section-story-wallframe.svelte';
    import Event from '../sections/section-event-wallframe.svelte';
    import Maps from '../sections/section-maps-wallframe.svelte';
    import Gift from '../sections/section-gift-wallframe.svelte';
    import Wish from '../sections/section-wish-wallframe.svelte';
    import Livestream from '../sections/section-livestream-wallframe.svelte';
    import Dresscode from '../sections/section-dresscode-wallframe.svelte';
    import Gallery from '../sections/section-gallery-wallframe.svelte';
    import Thanks from '../sections/section-thanks-wallframe.svelte';

    let showStory = true;
    let showEvent = true;
</script>
<main class="max-w-2xl mx-auto bg-[#B0A695] text-[#EBE3D5] relative" style="background-image:url(/texturewallframeindex.png); background-size: contain; background-position: center; background-repeat: repeat-y; font-family: 'Cormorand Garamond Regular';">
    <Opening />
    <Quote />
    <Bride/>
    <Groom />

    <section class="relative overflow-hidden">
        {#if showStory && showEvent}
            <!-- Dua komponen ada → foto ditengah -->
            <div class="absolute top-1/2 -right-10 -translate-y-90 sm:-translate-y-1/2 flex justify-center z-1 w-[75%] sm:w-[62.5%]">
                <div class="bg-[#A29683]/30 w-full h-full absolute"></div>
                <img src="/bridegroomwallframe.png" alt="center image" class="w-full object-cover" />
            </div>
            <div class="absolute top-1/2 -right-30 -translate-y-100 sm:-translate-y-1/2 flex justify-center z-1 w-[100%] sm:w-[85%]">
                <img src="/storyeventframewallframe.png" alt="center image" class="w-full object-cover" />
            </div>
        {:else if showStory}
            <!-- Hanya Story → foto di kanan atas -->
            <div class="absolute bottom-0 right-0 translate-y-1/2 flex justify-center z-1 w-[80%] sm:w-[62.5%] sm:h-auto">
                <div class="bg-[#A29683]/30 w-full h-full absolute"></div>
                <img src="/bridegroomwallframe.png" alt="center image" class="w-full object-cover" />
            </div>
        {:else if showEvent}
            <!-- Hanya Event → foto di kanan bawah -->
            <div class="absolute top-0 right-0 -translate-y-1/2 flex justify-center z-1 w-[80%] sm:w-[62.5%]">
                <div class="bg-[#A29683]/30 w-full h-full absolute"></div>
                <img src="/bridegroomwallframe.png" alt="center image" class="w-full object-cover" />
            </div>
        {/if}

        {#if showStory}
            <Story />
        {/if}

        {#if showEvent}
            <Event />
        {/if}
    </section>

    <Maps />
    <Gift />
    <Wish />
    <Livestream />
    <Dresscode />
    <Gallery />
    <Thanks />
</main>