<script>
    function handleRedirect(){
        window.location.href = ('/blueframe');
    }
</script>

<div class="min-h-screen sm:min-h-[1195px] relative pt-45">
    <!-- content -->
    <div class="bg-blue-950 w-[90%] ml-auto flex flex-col items-center py-5 z-3 relative">
        <h1 class="uppercase text-3xl sm:text-4xl" style="font-family: 'Fleischmen Regular';">Sabrina & Arthur</h1>
        <h2 class="text-2xl sm:text-3xl mt-1 sm:mt-5">Dear Alan and Partner</h2>
    </div>
    <button class="absolute bottom-14 left-10 bg-blue-950 text-lg sm:text-2xl px-7 py-3 sm:py-5 z-4 border border-blue-950 hover:bg-transparent hover:text-blue-950 transition cursor-pointer" on:click={handleRedirect}>
        Open Invitation
    </button>
    <div class="absolute top-0 left-0 w-[204px] h-[527px] sm:w-[319px] sm:h-[533px]">
        <img src="topleftlandingblueframe.png" alt="" class="h-full w-full object-cover">
    </div>
    <div class="absolute top-0 right-5 sm:right-10 w-[170px] h-[155px] sm:w-[259px] sm:h-[119px]">
        <img src="img2landingblueframe.png" alt="" class="h-full w-full object-cover">
    </div>
    <div class="absolute bottom-0 right-0 w-[372px] h-[559px] sm:w-[549px] sm:h-[824px] z-2">
        <img src="landingpictblueframe.png" alt="" class="h-full w-full object-cover">
    </div>
</div>