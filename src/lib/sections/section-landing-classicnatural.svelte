<script>
    function handleRedirect(){
        window.location.href = ('/classicnatural');
    }
</script>

<div class="h-full min-h-screen sm:min-h-[1195px] relative flex flex-col items-center" style="font-family: 'Foglihten Regular';">
    <div class="h-[826px] w-full overflow-hidden bg-black">
        <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover object-bottom">
    </div>

    <div class="flex flex-col items-center text-center mt-15">
        <h1 class="uppercase text-5xl tracking-[0.15em] mb-8" style="font-family: 'Kenia Regular';">The Wedding Of</h1>
        <h3 class="text-3xl mb-4" style="font-family: 'Brittany Regular';">Hinata & Naruto</h3>
        <p class="text-center text-xl mb-5">Dear, <br>Alan and Partner</p>
        <button class="bg-[#C7C7B8] text-neutral-50 text-center text-base px-4 py-2 rounded-xl border border-[#C7C7B8] hover:bg-transparent hover:text-[#C7C7B8] transition" on:click={handleRedirect}>Open Invitation</button>
    </div>
</div>