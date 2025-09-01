<script>
  let dresscodeRules = [
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
    "PAKAIAN BERWARNA GOLD",
  ];
</script>

<div class="h-[932px] sm:h-[1195px] relative">

    <div class="border-3 border-neutral-950 h-full m-5 sm:m-8 flex flex-col items-center text-neutral-950">

        <h1 class="text-2xl sm:text-5xl tracking-[0.2em] mb-2 sm:mb-3 border-b-3 border-[#878C7B] pb-3 mt-10 sm:mt-20" style="font-family: 'Kenia Regular';">DRESSCODE</h1>
        <p class="text-xl mt-10">Semi-Formal</p>
        <p class="text-base sm:text-xl mt-10 px-10 text-center">We invite guests to dress in our color palette for beautiful photos</p>
        <!-- Color Palette -->
        <div class="flex justify-center my-5 sm:my-10">
            <div class="w-12 h-12 sm:w-16 sm:h-16 bg-[#ececef] border border-neutral-50"></div>
            <div class="w-12 h-12 sm:w-16 sm:h-16 bg-[#e2e2e6] border border-neutral-50"></div>
            <div class="w-12 h-12 sm:w-16 sm:h-16 bg-[#bdbdc7] border border-neutral-50"></div>
            <div class="w-12 h-12 sm:w-16 sm:h-16 bg-[#8c8c97] border border-neutral-50"></div>
        </div>
        <p class="text-base sm:text-xl sm:mt-10 px-5 sm:px-10 text-center">guests are expected to wear clothes that are more polite and classy than everyday clothes, do not wear ;</p>
        <!-- dresscode rules -->
        <div class="grid grid-cols-2 md:grid-cols-2 gap-2 sm:gap-4 mt-4 sm:mt-8 sm:px-4 md:px-0" style="font-family: 'Cinzel Regular', serif;">
            {#each dresscodeRules.slice(0, dresscodeRules.length % 2 === 0 ? dresscodeRules.length : dresscodeRules.length - 1) as rule}
                <div class="bg-neutral-50 border border-neutral-50 text-neutral-950 transition py-1 px-2 sm:px-3 text-center text-[10px] sm:text-base rounded-lg cursor-pointer" style="font-family: 'Cinzel Regular';">
                    {rule}
                </div>
            {/each}
            {#if dresscodeRules.length % 2 === 1}
                <div class="bg-neutral-50 border border-neutral-50 rounded-lg transition py-1 text-center text-[10px] sm:text-base col-span-2 mx-auto w-1/2 text-neutral-950 cursor-pointer" style="font-family: 'Cinzel Regular';">
                    {dresscodeRules[dresscodeRules.length - 1]}
                </div>
            {/if}
        </div>
    </div>

    <div class="absolute bottom-0 flex flex-row w-full items-end gap-2">
        <div class="w-full h-[350px] sm:h-[388px]">
            <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
        </div>
        <button class="text-neutral-50 absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 rounded-full p-1 hover:bg-black/20 transition z-10" aria-label="Play Video">
            <svg class="w-full h-auto max-w-[39px]" viewBox="0 0 39 39" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
                <path d="M34.7747 7.38404C31.2086 2.88617 25.6875 0 19.4998 0C8.7311 0 0 8.73204 0 19.5C0 30.2688 8.73196 39 19.4998 39C26.5847 39 32.7861 35.2211 36.1965 29.5704C37.9776 26.6322 39 23.1829 39 19.4991C39 14.923 37.4229 10.7103 34.775 7.38249L34.7747 7.38404ZM27.2094 20.5698L16.9593 27.9354C16.7325 28.0983 16.4677 28.184 16.1932 28.184C15.4652 28.184 14.8731 27.5923 14.8731 26.8653V12.1347C14.8731 11.4076 15.4651 10.8159 16.1932 10.8159C16.4681 10.8159 16.7328 10.9016 16.9593 11.0642L27.2094 18.4301C27.5531 18.6771 27.758 19.0772 27.758 19.4999C27.7577 19.923 27.5524 20.3226 27.2094 20.5698Z" 
                fill="currentColor" />
            </svg>
        </button>
    </div>
</div>