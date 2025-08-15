<script lang="ts">
  import { landingpages } from '$lib/landingpages.js';
  import { ScrollArea } from "$lib/components/ui/scroll-area/index.js";
</script>
<div class="bg-neutral-50 flex flex-col justify-between h-screen w-8/48 py-6 sticky top-0 border-r-1" style="font-family: 'RethinkSans-Medium', sans-serif;">
    <div>
        <!-- {{-- BRAND NAME --}} -->
        <div class="flex items-center mb-6 pb-5 border-b border-gray-200 w-full px-8">
            <a href="#top" class="mr-2 text-2xl font-semibold flex items-center cursor-pointer">Sendvitation</a>
        </div>
        <ScrollArea class="w-full h-90 pb-7 border-b border-gray-200">
            <ul class="space-y-1 px-8">
                {#each landingpages as lp, i}
                    <li>
                        <a href={"#"+lp.id} class="flex flex-col items-baseline justify-between cursor-pointer"
                            on:click|preventDefault={() => {
                                const el = document.getElementById(lp.id);
                                if (el) el.scrollIntoView({ behavior: 'smooth' });
                            }}>
                            <span class="font-medium text-lg">{lp.name}</span>
                            <span class="text-base text-gray-400">{String(i+1).padStart(2, '0')}</span>
                        </a>
                    </li>
                {/each}
            </ul>
        </ScrollArea>
    </div>
</div>
