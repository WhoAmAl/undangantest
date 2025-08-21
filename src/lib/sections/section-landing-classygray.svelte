<script>
    function handleRedirect() {
        window.location.href = '/classygray';
    }
</script>

<div class="min-h-[1195px] flex justify-center relative" style="background-image: url(/coverclassygray.png); background-size: cover; background-position: center; background-repeat: no-repeat; font-family: 'Cinzel Regular', serif;">
    <!-- THE Wedding OF -->
    <div class="mt-30">
        <h1 class="text-4xl md:text-5xl font-light tracking-widest text-neutral-900">
            THE <span class="italic font-script text-5xl md:text-6xl text-neutral-50" style="font-family: 'Brittany', cursive;">Wedding</span> OF
        </h1>
    </div>
    <!-- section bawah -->
    <div class="bottom-0 absolute justify-center flex flex-col items-center w-full text-neutral-50 gap-8">
        <!-- Couple Names -->
        <div>
            <h2 class="text-6xl md:text-5xl font-script italic text-white" style="font-family: 'Brittany', cursive;">
                Hinata & Naruto
            </h2>
        </div>

        <!-- Dear Section -->
        <div class="text-center" style="font-family: 'Cinzel Regular', serif;">
            <p class="text-xl md:text-2xl tracking-wider mb-4">DEAR :</p>
            <p class="text-2xl md:text-[22px] tracking-wide">ALAN AND PARTNER</p>
        </div>

        <!-- Open Invitation Button -->
        <div class="mb-20" style="font-family: 'Cinzel Regular', serif;">
            <button class="border-2 border-white px-3 py-1.5 text-lg md:text-lg font-light tracking-wider hover:bg-white hover:text-neutral-900 transition-colors duration-300" on:click={handleRedirect}>
                OPEN INVITATION
            </button>
        </div>
    </div>
</div>