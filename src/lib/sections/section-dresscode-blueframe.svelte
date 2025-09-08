<script>
    let wearnots = [
        "Kaos Oblong", 
        "Sendal Jepit", 
        "Celana Pendek",
        "Pakaian Berwarna Gold",
        "Pakaian Terbuka",
    ];
</script>

<div class="relative flex flex-col">
    <div class="absolute w-[323px] h-[323px] sm:w-[497px] sm:h-[497px] translate-x-4/24 -translate-y-35 sm:-translate-y-40">
        <img src="/img1dresscodeblueframe.png" alt="" class="w-full h-full object-cover">
    </div>

    <div class="bg-blue-950 py-7 sm:py-9 px-10 sm:px-15 w-fit z-1 relative mt-15">
        <h1 class="text-blue-100 uppercase text-4xl sm:text-5xl" style="font-family: 'GFS Fleischman';">Dresscode</h1>
    </div>
    <h1 class="text-lg sm:text-xl text-blue-950 mx-auto text-center px-6 sm:px-30 mt-10 sm:mt-45">Kami harap Anda dapat mengenakan apa pun yang Anda suka. Jika Anda memiliki permintaan khusus, silakan beritahu kami.</h1>
    <h1 class="text-center text-lg sm:text-xl mt-5 text-blue-950">Color Recommendation</h1>
    <div class="flex flex-row gap-4 justify-center mt-2 sm:mt-5 z-1">
        <span class="bg-blue-950 w-[60px] h-[60px] sm:w-[74px] sm:h-[74px]"></span>
        <span class="bg-blue-900 w-[60px] h-[60px] sm:w-[74px] sm:h-[74px]"></span>
        <span class="bg-blue-800 w-[60px] h-[60px] sm:w-[74px] sm:h-[74px]"></span>
        <span class="bg-blue-300 w-[60px] h-[60px] sm:w-[74px] sm:h-[74px]"></span>
    </div>
    <div class="bg-blue-950 mb-20 flex flex-col px-6 sm:px-20 text-center w-[383px] sm:w-[463px] h-[166px] py-5 ml-auto mt-15 sm:mt-30 z-1" style="font-family: 'Questrial';">
        <h1 class="text-xl">Jangan gunakan :</h1>
        <div class="flex flex-row flex-wrap gap-5 w-[330px] mt-5 justify-center">
            {#each wearnots as wear}
                <p class="leading-tight text-base">{wear}</p>
            {/each}
        </div>
    </div>
    <div class="absolute bottom-0 w-[151px] h-[404px] sm:w-[322px] sm:h-[536px] translate-y-30 sm:translate-y-62">
        <img src="/img2dresscodeblueframe.png" alt="" class="w-full h-full object-cover">
    </div>
</div>