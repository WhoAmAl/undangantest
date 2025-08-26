<script>
    function handleRedirect() {
        window.location.href = '/naturalgreen';
    }
</script>

<div class="min-h-screen flex flex-col items-center py-15" style="font-family: 'Hahmlet Regular';">
    <!-- header -->
    <div class="text-center items-center flex flex-col mb-15">
        <h1 class="uppercase text-6xl" style="font-family: 'Bacasime Antique Regular';">The Wedding Of</h1>
        <span class="text-[32px]">23.08.2025</span>
    </div>

    <!-- central -->
    <div class="flex flex-row items-center justify-center">
        <h2 class="-rotate-90 h-fit text-6xl translate-x-15 leading-0 -translate-y-45" style="font-family: 'Thank You Regular';">Sabrina</h2>
        
        <!-- img -->
        <div class="p-3 w-[454px] h-[622px] border border-green-900 rounded-2xl -translate-x-4">
            <img src="/covernaturalgreen.png" alt="" class="object-center object-cover h-full w-full rounded-xl">
        </div>
        <h2 class="-rotate-90 h-fit text-6xl -translate-x-15 leading-0 translate-y-50" style="font-family: 'Thank You Regular';">Arthur</h2>
    </div>

    <!-- under img -->
    <div class="flex flex-col items-center mt-20">
        <h1 class="text-xl mb-5">Dear,</h1>
        <h2 class="text-3xl mb-10">Alan & Partner</h2>
        <button class="bg-green-900 rounded-xl py-2 px-4 text-base text-lime-50 hover:bg-lime-50 hover:text-green-900 hover:border hover:border-green-900 transition" on:click={handleRedirect}>Open Invitation</button>
    </div>
</div>