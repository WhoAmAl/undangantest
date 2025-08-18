<script lang="ts">
    import * as Carousel from "$lib/components/ui/carousel/index.js";

    let giftRecommendations = [
        {
            name: "Cermin",
            icon: `<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"40\" height=\"40\" fill=\"#888\" viewBox=\"0 0 24 24\"><path d=\"M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z\"/></svg>`
        },
        {
            name: "Bedcover",
            icon: `<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"40\" height=\"40\" fill=\"#888\" viewBox=\"0 0 24 24\"><path d=\"M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z\"/></svg>`
        },
        {
            name: "Kulkas",
            icon: `<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"40\" height=\"40\" fill=\"#888\" viewBox=\"0 0 24 24\"><path d=\"M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z\"/></svg>`
        },
        {
            name: "Kulkas",
            icon: `<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"40\" height=\"40\" fill=\"#888\" viewBox=\"0 0 24 24\"><path d=\"M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z\"/></svg>`
        },
        {
            name: "Kulkas",
            icon: `<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"40\" height=\"40\" fill=\"#888\" viewBox=\"0 0 24 24\"><path d=\"M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z\"/></svg>`
        },
        {
            name: "Kulkas",
            icon: `<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"40\" height=\"40\" fill=\"#888\" viewBox=\"0 0 24 24\"><path d=\"M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z\"/></svg>`
        }
    ];
</script>

<div class="bg-[#6F7B95] flex flex-col items-center text-gray-200 px-3 sm:px-10">
    <h1 class="text-4xl sm:text-6xl mt-10" style="font-family: 'Great Vibes Regular', serif;">Gift</h1>

    <p class="text-center mt-4 sm:mt-12 text-base sm:text-2xl">If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful</p>

    <!-- GIFTS -->
    <div class="flex flex-col justify-center items-center mt-10 bg-gray-200/50 py-5 px-2 sm:px-15 rounded-2xl w-full">
        <h1 class="text-[#223B59] text-4xl" style="font-family: 'Zilla Slab', serif;">Cashless</h1>
        <div class="flex flex-col sm:flex-row items-center justify-between w-full ">
            <div class="flex flex-col items-center p-5">
                <img src="/BCA.png" alt="BCA" class="w-auto h-8">
                <p class="mt-2 text-gray-800 text-2xl">Hinata</p>
                <p class="text-gray-600 text-xl">123456789</p>
                <button class="mt-2 bg-gray-200 text-gray-800 px-4 py-1 rounded-full">Copy to clipboard</button>
            </div>
            <div class="flex flex-col items-center p-5">
                <img src="/BCA.png" alt="BCA" class="w-auto h-8">
                <p class="mt-2 text-gray-800 text-2xl">Naruto</p>
                <p class="text-gray-600 text-xl">123456789</p>
                <button class="mt-2 bg-gray-200 text-gray-800 px-4 py-1 rounded-full">Copy to clipboard</button>
            </div>
        </div>
        <div class="flex flex-col items-center mt-5 sm:mt-10 rounded-lg pb-5">
            <p class="text-gray-800 text-3xl" style="font-family: 'Zilla Slab', serif;">Gift</p>
            <p class="text-gray-600 text-xl text-center">Orchid Streat Number 15, West Jakarta</p>
            <button class="mt-2 bg-gray-200 text-gray-800 px-8 py-1 rounded-full">Copy address</button>
        </div>
    </div>

    <!-- RECOMMENDED GIFT -->
    <div class="text-gray-200 w-full sm:mt-4 flex flex-col items-center relative">
        <h1 class="text-3xl sm:text-4xl my-5" style="font-family: 'Zilla Slab', serif;">Gift Recommendation</h1>
        <!-- Grid Cards: hanya tampil di sm ke atas -->
        <div class="hidden sm:grid grid-cols-3 justify-items-center w-full px-6 gap-x-6 mb-0">
            {#each giftRecommendations as gift}
                <div class="rounded-xl w-64 h-72 flex flex-col items-center justify-between pb-10">
                    <div class="flex-1 flex items-center justify-center">
                        <div class="bg-neutral-400 w-40 h-40 flex items-center justify-center rounded-2xl">
                            {@html gift.icon}
                        </div>
                    </div>
                    <div class="text-lg mt-1 mb-1 text-center">{gift.name}</div>
                    <button class="bg-gray-200 text-[#223B59] px-8 py-1 hover:bg-neutral-200 transition mb-2 rounded-full">Lihat Detail</button>
                </div>
            {/each}
        </div>
        <!-- Carousel: hanya tampil di bawah sm -->
        <div class="flex sm:hidden w-full px-2 justify-center">
            <Carousel.Root
                opts={{
                    align: "start"
                }}
                orientation="vertical"
                class="w-full max-w-xs"
            >
                <Carousel.Content class="-mt-1 h-[300px]">
                    {#each Array(Math.ceil(giftRecommendations.length/2)) as _, i (i)}
                    <Carousel.Item class="pt-1 md:basis-1/2">
                        <div class="flex flex-row gap-4 justify-center">
                            <!-- Card 1 -->
                            {#if giftRecommendations[i*2]}
                            <div class="w-64 h-72 flex flex-col items-center justify-between py-6">
                                <div class="flex-1 flex items-center justify-center">
                                    <div class="bg-neutral-400 w-40 h-40 flex items-center justify-center">
                                        {@html giftRecommendations[i*2].icon}
                                    </div>
                                </div>
                                <div class="text-gray-200 text-lg mt-4 mb-1 text-center">{giftRecommendations[i*2].name}</div>
                                <button class="bg-gray-200 text-[#223B59] px-7 py-1.5 hover:bg-neutral-200 transition mb-2">Lihat Detail</button>
                            </div>
                            {/if}
                            <!-- Card 2 -->
                            {#if giftRecommendations[i*2+1]}
                            <div class="w-64 h-72 flex flex-col items-center justify-between py-6">
                                <div class="flex-1 flex items-center justify-center">
                                    <div class="bg-neutral-400 w-40 h-40 flex items-center justify-center">
                                        {@html giftRecommendations[i*2+1].icon}
                                    </div>
                                </div>
                                <div class="text-gray-200 text-lg mt-4 mb-1 text-center">{giftRecommendations[i*2+1].name}</div>
                                <button class="bg-gray-200 text-[#223B59] px-7 py-1.5 hover:bg-neutral-200 transition mb-2">Lihat Detail</button>
                            </div>
                            {/if}
                        </div>
                    </Carousel.Item>
                    {/each}
                </Carousel.Content>
            </Carousel.Root>
        </div>
    </div>
</div>