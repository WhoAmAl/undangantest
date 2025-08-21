<script>
  let dresscodeRules = [
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
  ];
</script>

<div class="text-neutral-50 min-h-screen sm:min-h-[1195px] flex flex-col items-center relative sm:pt-30 sm:px-10" style="background-image: url(/coverclassygray.png); background-size: cover; background-position: center; background-repeat: no-repeat;">
    <!-- TITLE -->
    <div class="bg-neutral-900/75 border-b-1 border-neutral-50 w-full h-full">
        <h1 class="text-center text-2xl sm:text-5xl py-1 sm:py-2">DRESSCODE</h1>
    </div>

    <!-- body content -->
    <div class="bg-neutral-900/75 min-h-screen sm:min-h-0 flex flex-col items-center w-full pt-10 pb-11 sm:pb-4 px-4 sm:mt-40" style="font-family: 'Cormorand Garamond Regular', serif;">
        <!-- Subtitle -->
        <div class="text-center text-2xl sm:text-3xl mb-6" style="font-family: 'Foglihten Regular';">Semi-Formal</div>
        <!-- Invitation Text -->
        <div class="text-center text-lg sm:text-xl mb-8 max-w-2xl mx-auto">
            We invite guests to dress in our color palette for beautiful photos
        </div>
        <!-- Color Palette -->
        <div class="flex justify-center mb-8">
            <div class="w-16 h-16 bg-[#ececef] border border-neutral-50"></div>
            <div class="w-16 h-16 bg-[#e2e2e6] border border-neutral-50"></div>
            <div class="w-16 h-16 bg-[#bdbdc7] border border-neutral-50"></div>
            <div class="w-16 h-16 bg-[#8c8c97] border border-neutral-50"></div>
        </div>
        <!-- Expectation Text -->
        <div class="text-center text-lg sm:text-xl mb-8 max-w-2xl mx-auto">
            guests are expected to wear clothes that are more polite and classy than everyday clothes, do not wear ;
        </div>
        <!-- dresscode rules -->
        <div class="grid grid-cols-2 md:grid-cols-2 gap-4 mt-8 sm:px-4 md:px-0" style="font-family: 'Cinzel Regular', serif;">
            {#each dresscodeRules.slice(0, dresscodeRules.length % 2 === 0 ? dresscodeRules.length : dresscodeRules.length - 1) as rule}
                <div class="bg-transparent border border-neutral-50 text-neutral-50 py-1 text-center text-xs sm:text-base px-3">
                    {rule}
                </div>
            {/each}
            {#if dresscodeRules.length % 2 === 1}
                <div class="bg-transparent border border-neutral-50 text-neutral-50 py-1 text-center text-xs sm:text-base px-3 col-span-2 mx-auto w-1/2">
                    {dresscodeRules[dresscodeRules.length - 1]}
                </div>
            {/if}
        </div>
    </div>
</div>