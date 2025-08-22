<script>
  let dresscodeRules = [
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
  ];
</script>

<div class="min-h-screen sm:min-h-[1195px] relative" style="background-image: url(/covercleangray.png); background-size: cover; background-position: center; background-repeat: no-repeat;">
    <div class="absolute inset-0 bg-slate-500/50 items-center justify-center flex flex-col text-neutral-50 px-3 sm:px-6" style="font-family: 'Cormorant Garamond Regular';">
        <div class="border-4 border-neutral-50 pb-5 sm:pb-20 pt-5 px-2 sm:px-8">
            <!-- Title -->
            <div class="text-center text-2xl sm:text-6xl mb-10 sm:mb-25" style="font-family: 'Abhaya Regular';">DRESSCODE</div>
            <!-- Subtitle -->
            <div class="text-center text-2xl sm:text-3xl mb-6 font-extralight">Semi-Formal</div>
            <!-- Invitation Text -->
            <div class="text-center text-lg sm:text-2xl mb-8 mx-auto">
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
            <div class="text-center text-base sm:text-2xl mb-8 mx-auto sm:px-4">
                guests are expected to wear clothes that are more polite and classy than everyday clothes, do not wear ;
            </div>
            <!-- dresscode rules -->
            <div class="grid grid-cols-2 md:grid-cols-2 gap-4 mt-8 sm:px-4 md:px-0" style="font-family: 'Cinzel Regular', serif;">
                {#each dresscodeRules.slice(0, dresscodeRules.length % 2 === 0 ? dresscodeRules.length : dresscodeRules.length - 1) as rule}
                    <div class="bg-slate-300 border border-slate-700 text-slate-700 transition py-1 text-center text-[10px] sm:text-base hover:shadow-[0_6px_0_0_rgba(51,65,85,1)]  active:shadow-[0_1px_0_0_rgba(51,65,85,1)] active:translate-y-1 rounded-3xl cursor-pointer" style="font-family: 'Cormorant Garamond Bold';">
                        {rule}
                    </div>
                {/each}
                {#if dresscodeRules.length % 2 === 1}
                    <div class="bg-slate-300 border border-slate-700 rounded-3xl transition py-1 text-center text-[10px] sm:text-base col-span-2 mx-auto w-1/2 text-slate-800 hover:shadow-[0_6px_0_0_rgba(51,65,85,1)]  active:shadow-[0_1px_0_0_rgba(51,65,85,1)] active:translate-y-1 cursor-pointer" style="font-family: 'Cormorant Garamond Bold';">
                        {dresscodeRules[dresscodeRules.length - 1]}
                    </div>
                {/if}
            </div>
        </div>
    </div>
</div>