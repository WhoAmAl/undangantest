<script>
    function handleRedirect() {
        window.location.href = "/botanical";
    }
</script>

<div class="flex flex-col items-center bg-neutral-50 pt-12 relative min-h-screen" style="font-family: 'Gentium Plus Regular', serif;">
    <h2 class="text-fuchsia-900 text-lg md:text-2xl tracking-[0.2em] uppercase mb-8" style="font-family: 'Uchen Regular', serif;">WE'RE GETTING MARRIED</h2>
    <div class="relative flex flex-col items-center">
        <img src="/bridegroombotanic.png" alt="Couple" class="w-60 md:w-100 h-auto object-cover rounded-full" />
        <img src="/lavenderlandingbotanical.png" alt="Lavender Flowers" class="absolute -bottom-10 md:-bottom-20 left-1/2 -translate-x-1/2 pointer-events-none z-10 max-w-none w-[100vw] md:w-[25vw]"/>
    </div>
    <button class="mt-15 md:mt-25 bg-fuchsia-900 text-white rounded-md md:rounded-xl px-3 md:px-5 py-1 md:py-2 text-[12px] md:text-base shadow-lg hover:bg-purple-900 transition" on:click={handleRedirect}>Open Invitation</button>
    <h1 class="text-fuchsia-900 text-2xl md:text-5xl mt-2 md:mt-10 md:mb-8 text-center" style="font-family: 'Oleo Script Swash Regulars', cursive;">Hinata &amp; Naruto</h1>
    <div class="text-fuchsia-900 text-xs md:text-xl tracking-[0.3em] uppercase mb-8 text-center" style="font-family: 'Uchen Regular', serif;">DEAR ALAN &amp; PARTNER</div>
    <img src="/bungabawahlanding.png" alt="Bottom Lavender" class="w-full max-w-none pointer-events-none select-none absolute left-0 bottom-0" style="height:auto;" />
</div>