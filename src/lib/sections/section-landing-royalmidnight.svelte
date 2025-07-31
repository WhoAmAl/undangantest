<script>
    import { goto } from '$app/navigation';

    function handleRedirect() {
        goto('/royalmidnight');
    }
</script>

<div class="bg-[#172554] max-w-2xl min-h-screen sm:min-h-screen mx-auto flex flex-col items-center relative">
    <h1 class="font-['Foglihten-Regular'] text-white text-xl sm:text-4xl tracking-widest text-center mt-12 sm:mt-18">
        PLEASE JOIN US !
    </h1>
    <div class="flex-1 flex items-center justify-center w-full">
        <img src="/coverroyalmidnight.png" alt="" class="mt-3 shadow-2xl max-w-[55vw] max-h-[450vw] sm:max-w-[382px] sm:max-h-none rounded-t-full rounded-b-full" />
    </div>
    <!-- nama bride & groom -->
    <div class="font-['Ms_Madi'] text-white text-3xl sm:text-5xl font-light text-center flex flex-col items-center gap-1 sm:gap-2 mb-10 sm:mb-20">
        <span>Naruto</span>
        <span class="text-2xl sm:text-3xl">&amp;</span>
        <span>Hinata</span>
    </div>

    <!-- Button -->
    <button 
        on:click={handleRedirect}
        class="bg-white text-[#172554] border-none px-6 py-2 sm:px-8 sm:py-3 rounded-xl text-xs sm:text-sm tracking-wider cursor-pointer transition-all duration-300 sm:mb-6 shadow-lg hover:bg-gray-100  hover:shadow-xl active:translate-y-0 -translate-y-[28px] sm:-translate-y-[60px] sm:active:translate-y-0" 
        style="font-family: 'Cormorant Upright', serif;"
    >
        Open Invitation
    </button>
    <!-- Hiasan bunga pojok kiri bawah -->
    <img 
        src="/leftbottomroyalmidnight.png" 
        alt="Bunga pojok kiri bawah" 
        class="absolute left-0 bottom-0 h-[22.5%] sm:h-[22.5%]"
    />
    <!-- Hiasan bunga pojok kanan bawah (mirror) -->
    <img 
        src="/leftbottomroyalmidnight.png" 
        alt="Bunga pojok kanan bawah" 
        class="absolute right-0 bottom-0 h-[22.5%] sm:h-[22.5%]"
        style="transform: scaleX(-1);"
    />
</div>