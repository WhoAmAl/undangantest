<script>
    let imgs = [
        '/landingpictblueframe.png',
        '/landingpictblueframe.png',
        '/landingpictblueframe.png',
        '/landingpictblueframe.png',
        '/landingpictblueframe.png',
        '/landingpictblueframe.png',
    ];
</script>

<div class="sm:min-h-[1145px] relative flex flex-col" style="font-family: 'Questrial';">
    <h1 class="ml-auto mr-3 sm:mr-10 text-4xl sm:text-5xl text-blue-950 mt-10 uppercase" style="font-family: 'GFS Fleischman';">Our <span style="font-family: 'Questrial';">Gallery</span></h1>
    <div class="ml-auto w-[396px] h-[257px] sm:w-[588px] sm:h-[382px] mt-10">
        <img src="/landingpictblueframe.png" alt="" class="w-full h-full object-cover">
    </div>
    <div class="grid grid-cols-3 gap-5 sm:gap-8 mt-10">
    {#each imgs as image}
        <div class="h-[149px] sm:h-[248px]">
            <img src={image} alt="" class="w-full h-full object-cover">
        </div>
    {/each}
    </div>

</div>