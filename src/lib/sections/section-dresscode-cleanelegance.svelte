<script>
  let dresscodeRules = [
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
  ];
</script>

<div class="bg-neutral-50 flex flex-col items-center text-yellow-950">
    <div class="border-t-3 border-yellow-950 w-[90%] mt-6 md:mt-12 z-1 mb-4 md:mb-6"></div>
    <!-- Content Top -->
    <div class="w-full px-8 md:px-12">
        <div class="bg-yellow-950 py-2 md:py-4 px-2 text-center w-full">
            <span class="text-3xl md:text-5xl text-gray-50" style="font-family: 'Tangerine Regular', serif;">Dresscode</span>
        </div>
    </div>
    <div class="px-8 sm:px-16">
        <div class="pt-8 md:pt-12 text-center text-base md:text-lg">Semi-Formal</div>
        <div class="mt-8 text-center text-lg md:text-xl sm:px-4 md:px-0" style="color:#4a2a0a;">
            We invite guests to dress in our color palette for beautiful photos
        </div>
        <div class="flex justify-center mt-6 mb-6">
            <div class="flex gap-1">
                <div class="w-12 h-12 md:w-16 md:h-16" style="background:#ecebeb;"></div>
                <div class="w-12 h-12 md:w-16 md:h-16" style="background:#e2e1e1;"></div>
                <div class="w-12 h-12 md:w-16 md:h-16" style="background:#bdbbc0;"></div>
                <div class="w-12 h-12 md:w-16 md:h-16" style="background:#8c8a8e;"></div>
            </div>
        </div>
        <div class="mt-2 text-center text-base sm:text-[22px] font-normal px-4 md:px-0" style="color:#4a2a0a;">
            guests are expected to wear clothes that are more polite and classy than everyday clothes, do not wear ;
        </div>
        <!-- dresscode rules -->
        <div class="grid grid-cols-2 md:grid-cols-2 gap-4 mt-8 sm:px-4 md:px-0">
            {#each dresscodeRules.slice(0, dresscodeRules.length % 2 === 0 ? dresscodeRules.length : dresscodeRules.length - 1) as rule}
                <div class="bg-yellow-950 text-neutral-50 py-1 text-center text-xs sm:text-base px-1">
                    {rule}
                </div>
            {/each}
            {#if dresscodeRules.length % 2 === 1}
                <div class="bg-yellow-950 text-neutral-50 py-1 text-center text-xs sm:text-base px-1 col-span-2 mx-auto w-1/2">
                    {dresscodeRules[dresscodeRules.length - 1]}
                </div>
            {/if}
        </div>
    </div>

    <div class="border-t-3 border-yellow-950 w-[90%] mt-6 md:mt-14 z-1 mb-4 md:mb-8"></div>
</div>
