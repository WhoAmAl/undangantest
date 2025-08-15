<div class="h-screen flex flex-col items-center justify-between">
    <!-- row 1 -->
    <div class="flex flex-row sm:flex-col w-full bg-neutral-50 flex-1 overflow-hidden justify-between sm:items-center">
        <!-- wedding ceremony -->
        <div class="px-4 text-center text-yellow-950 w-1/2 sm:w-full">
            <div class="text-2xl sm:text-4xl mt-5 sm:mt-10" style="font-family: 'Tangerine Regular', serif;">Wedding Ceremony</div>
            <div class="w-full border-t border-yellow-950 mt-1 sm:mt-3"></div>
            <div class="flex flex-row items-end justify-center gap-2 mt-2 sm:mt-8 mb-2 sm:mb-6">
                <span class="text-lg sm:text-2xl">July</span>
                <span class="text-2xl sm:text-5xl">05</span>
                <span class="text-lg sm:text-2xl">2025</span>
            </div>
            <div class="text-[18px] sm:text-[22px] mb-2 sm:mb-6">Pukul: 09.00 Wib s/d Selesai</div>
            <div class="text-lg sm:text-xl mb-4">Grand Plaza Hotel</div>
            <div class="text-[14px] sm:text-lg mb-20 leading-tight sm:px-4">JENDRAL SUDIRMAN STREET KAV 52-53, KEBAYORAN BARU, SENAYAN, JAKARTA</div>
            <button
                class="py-2 px-4 bg-yellow-950 text-neutral-50 text-lg mt-2"
                on:click={() => window.open('https://maps.google.com/?q=Grand+Plaza+Hotel+Jakarta', '_blank', 'noopener')}
            >
                GOOGLE MAPS
            </button>
        </div>
        <!-- picture -->
        <div class="w-1/2 sm:w-full items-center justify-center">
            <img src="/bgcovercleanelegance.png" alt="" class="sm:mx-auto">
        </div>
    </div>
    <!-- row 2 -->
    <div class="flex flex-row sm:flex-col w-full bg-yellow-950 flex-1 overflow-hidden justify-between text-neutral-50 sm:items-center">
        <!-- picture -->
        <div class="w-1/2 sm:w-full items-center justify-center">
            <img src="/bgcovercleanelegance.png" alt="" class="sm:mx-auto">
        </div>
        <!-- Wedding reception -->
        <div class="px-4 text-center w-1/2 sm:w-full">
            <div class="text-2xl sm:text-4xl mt-5 sm:mt-10" style="font-family: 'Tangerine Regular', serif;">Wedding Reception</div>
            <div class="w-full border-t border-neutral-50 mt-3"></div>
            <div class="flex flex-row items-end justify-center gap-2 mt-3 sm:mt-8 mb-2 sm:mb-6">
                <span class="text-lg  sm:text-2xl">July</span>
                <span class="text-2xl sm:text-5xl">05</span>
                <span class="text-lg  sm:text-2xl">2025</span>
            </div>
            <div class="text-[18px] sm:text-[22px] mb-2 sm:mb-6">Pukul: 09.00 Wib s/d Selesai</div>
            <div class="text-lg sm:text-xl mb-4">Grand Plaza Hotel</div>
            <div class="text-[14px] sm:text-lg mb-20 leading-tight sm:px-4">JENDRAL SUDIRMAN STREET KAV 52-53, KEBAYORAN BARU, SENAYAN, JAKARTA</div>
            <button
                class="py-2 px-4 text-yellow-950 bg-neutral-50 text-lg mt-2"
                on:click={() => window.open('https://maps.google.com/?q=Grand+Plaza+Hotel+Jakarta', '_blank', 'noopener')}
            >
                GOOGLE MAPS
            </button>
        </div>
    </div>
</div>