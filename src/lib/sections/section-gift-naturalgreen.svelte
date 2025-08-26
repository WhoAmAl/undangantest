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

<div class="bg-green-900 border border-lime-50 rounded-2xl items-center flex justify-center px-10 py-2 translate-y-7 w-[70%] mx-auto">
    <h1 class="uppercase text-center text-xl sm:text-4xl text-lime-50">Gift</h1>
</div>

<div class="min-h-screen bg-green-900 rounded-2xl mx-4 sm:mx-8 mb-10 sm:mb-15 flex flex-col items-center text-lime-50" style="font-family: 'Hahmlet Regular';">
    <div class="text-center mt-12 sm:mt-20 px-6 sm:px-10">
         <p class="text-[12px] sm:text-[20px]">If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful</p>
    </div>
    <div class="flex flex-col sm:flex-row items-center w-full sm:gap-4 px-3">
        <!-- Cashless -->
        <div class="flex flex-row sm:flex-col items-center pt-5 sm:pt-0 sm:py-5 sm:w-1/2 w-full">
            <!-- Rekening 1 -->
            <div class="rounded-lg sm:mb-4 w-full max-w-md flex flex-col items-center">
                <svg width="47" height="47" viewBox="0 0 47 47" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M13.7082 29.3751H19.5832C20.1026 29.3751 20.6007 29.1688 20.9679 28.8015C21.3352 28.4342 21.5415 27.9361 21.5415 27.4167C21.5415 26.8974 21.3352 26.3993 20.9679 26.032C20.6007 25.6647 20.1026 25.4584 19.5832 25.4584H13.7082C13.1888 25.4584 12.6907 25.6647 12.3234 26.032C11.9562 26.3993 11.7498 26.8974 11.7498 27.4167C11.7498 27.9361 11.9562 28.4342 12.3234 28.8015C12.6907 29.1688 13.1888 29.3751 13.7082 29.3751ZM37.2082 9.79175H9.7915C8.23336 9.79175 6.73903 10.4107 5.63725 11.5125C4.53548 12.6143 3.9165 14.1086 3.9165 15.6667V33.2917C3.9165 34.8499 4.53548 36.3442 5.63725 37.446C6.73903 38.5478 8.23336 39.1667 9.7915 39.1667H37.2082C38.7663 39.1667 40.2606 38.5478 41.3624 37.446C42.4642 36.3442 43.0832 34.8499 43.0832 33.2917V15.6667C43.0832 14.1086 42.4642 12.6143 41.3624 11.5125C40.2606 10.4107 38.7663 9.79175 37.2082 9.79175ZM39.1665 33.2917C39.1665 33.8111 38.9602 34.3092 38.5929 34.6765C38.2257 35.0438 37.7276 35.2501 37.2082 35.2501H9.7915C9.27212 35.2501 8.77401 35.0438 8.40675 34.6765C8.03949 34.3092 7.83317 33.8111 7.83317 33.2917V21.5417H39.1665V33.2917ZM39.1665 17.6251H7.83317V15.6667C7.83317 15.1474 8.03949 14.6493 8.40675 14.282C8.77401 13.9147 9.27212 13.7084 9.7915 13.7084H37.2082C37.7276 13.7084 38.2257 13.9147 38.5929 14.282C38.9602 14.6493 39.1665 15.1474 39.1665 15.6667V17.6251Z" 
                    fill="currentColor"
                />
                </svg>
                <div class="text-lime-50 text-base sm:text-lg sm:mb-1">BCA an Sabrina</div>
                <div class="text-lime-50 text-xs sm:text-base mb-2 sm:mb-3">123456789</div>
                <button class="text-xs sm:text-base bg-lime-50 text-green-900 px-4 sm:px-8 py-1 rounded-full hover:bg-green-900 hover:border hover:border-lime-50 hover:text-lime-50 transition" style="font-family: 'Baskervville', serif;" on:click={() => navigator.clipboard.writeText('123456789')}>Copy to clipboard</button>
            </div>
            <!-- Rekening 2 -->
            <div class="rounded-lg w-full max-w-md flex flex-col items-center sm:mt-5">
                <svg width="47" height="47" viewBox="0 0 47 47" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M13.7082 29.3751H19.5832C20.1026 29.3751 20.6007 29.1688 20.9679 28.8015C21.3352 28.4342 21.5415 27.9361 21.5415 27.4167C21.5415 26.8974 21.3352 26.3993 20.9679 26.032C20.6007 25.6647 20.1026 25.4584 19.5832 25.4584H13.7082C13.1888 25.4584 12.6907 25.6647 12.3234 26.032C11.9562 26.3993 11.7498 26.8974 11.7498 27.4167C11.7498 27.9361 11.9562 28.4342 12.3234 28.8015C12.6907 29.1688 13.1888 29.3751 13.7082 29.3751ZM37.2082 9.79175H9.7915C8.23336 9.79175 6.73903 10.4107 5.63725 11.5125C4.53548 12.6143 3.9165 14.1086 3.9165 15.6667V33.2917C3.9165 34.8499 4.53548 36.3442 5.63725 37.446C6.73903 38.5478 8.23336 39.1667 9.7915 39.1667H37.2082C38.7663 39.1667 40.2606 38.5478 41.3624 37.446C42.4642 36.3442 43.0832 34.8499 43.0832 33.2917V15.6667C43.0832 14.1086 42.4642 12.6143 41.3624 11.5125C40.2606 10.4107 38.7663 9.79175 37.2082 9.79175ZM39.1665 33.2917C39.1665 33.8111 38.9602 34.3092 38.5929 34.6765C38.2257 35.0438 37.7276 35.2501 37.2082 35.2501H9.7915C9.27212 35.2501 8.77401 35.0438 8.40675 34.6765C8.03949 34.3092 7.83317 33.8111 7.83317 33.2917V21.5417H39.1665V33.2917ZM39.1665 17.6251H7.83317V15.6667C7.83317 15.1474 8.03949 14.6493 8.40675 14.282C8.77401 13.9147 9.27212 13.7084 9.7915 13.7084H37.2082C37.7276 13.7084 38.2257 13.9147 38.5929 14.282C38.9602 14.6493 39.1665 15.1474 39.1665 15.6667V17.6251Z" 
                    fill="currentColor"
                />
                </svg>
                <div class="text-lime-50 text-base sm:text-lg sm:mb-1">BNI an Arthur</div>
                <div class="text-lime-50 text-xs sm:text-base mb-2 sm:mb-3">123456789</div>
                <button class="text-xs sm:text-base bg-lime-50 text-green-900 px-4 sm:px-8 py-1 rounded-full hover:bg-green-900 hover:border hover:border-lime-50 hover:text-lime-50 transition" style="font-family: 'Baskervville', serif;" on:click={() => navigator.clipboard.writeText('123456789')}>Copy to clipboard</button>
            </div>
        </div>
        <!-- Gift -->
        <div class="flex flex-col items-center justify-center w-1/2">
            <div class="text-lime-50 text-xl pt-5 md:pt-0 mb-2" style="font-family: 'Baskervville', serif;">Gift</div>
            <div class="rounded-lg w-full max-w-md flex flex-col items-center">
                <div class="text-lime-50 text-base sm:text-xl text-center sm:px-3 mb-2" style="font-family: 'Baskervville', serif;">Orchid Streat Number 15, West Jakarta</div>
                <button class="text-xs sm:text-base bg-lime-50 text-green-900 px-6 sm:px-8 py-1 rounded-full hover:bg-green-900 hover:border hover:border-lime-50 hover:text-lime-50 transition" style="font-family: 'Baskervville', serif;" on:click={() => navigator.clipboard.writeText('Orchid Streat Number 15, West Jakarta')}>Copy address</button>
            </div>
        </div>
    </div>
    <div class="mt-6 mb-2 text-lime-50 uppercase text-lg sm:text-xl text-center">
        Gift Recommendation
    </div>
    <!-- RECOMMENDED GIFT -->
    <div class="text-neutral-50 w-full flex flex-col items-center relative sm:px-4">
        <!-- Grid Cards: hanya tampil di sm ke atas -->
        <div class="hidden sm:grid grid-cols-3 justify-items-center w-full px-6 gap-x-6 mb-0 py-3" style="font-family: 'Cormorant Garamond Regular', serif;">
            {#each giftRecommendations as gift}
                <div class="rounded-xl w-64 h-72 flex flex-col items-center">
                    <div class="flex items-center justify-center">
                        <div class="bg-neutral-400 rounded-xl w-40 h-40 flex items-center justify-center">
                            {@html gift.icon}
                        </div>
                    </div>
                    <div class="text-2xl mt-1 text-center">{gift.name}</div>
                    <button class="text-base sm:text-xl hover:border hover:border-lime-50 hover:bg-green-900 hover:text-lime-50 rounded-3xl bg-lime-50 sm:py-0.5 px-5 transition text-green-900 " style="font-family: 'Cormorant Garamond Regular';">
                        Lihat Detail
                    </button>
                </div>
            {/each}
        </div>
        <!-- Carousel: hanya tampil di bawah sm -->
        <div class="flex sm:hidden w-full justify-center">
            <Carousel.Root
                opts={{
                    align: "start"
                }}
                orientation="vertical"
                class="w-full"
            >
                <Carousel.Content class="-mt-1 h-[280px] w-full">
                    {#each Array(Math.ceil(giftRecommendations.length/2)) as _, i (i)}
                    <Carousel.Item class="pt-1 md:basis-1/2">
                        <div class="flex flex-row gap-4 items-center justify-center">
                            <!-- Card 1 -->
                            {#if giftRecommendations[i*2]}
                            <div class="w-64 h-72 flex flex-col items-center justify-between py-6">
                                <div class="flex-1 flex items-center justify-center">
                                    <div class="bg-neutral-400 w-40 h-40 flex items-center justify-center rounded-xl">
                                        {@html giftRecommendations[i*2].icon}
                                    </div>
                                </div>
                                <div class="text-neutral-50 text-lg mt-4 mb-1 text-center">{giftRecommendations[i*2].name}</div>
                                <button class="text-base sm:text-xl hover:border hover:border-lime-50 hover:bg-green-900 hover:text-lime-50 rounded-3xl bg-lime-50 sm:py-0.5 px-5 transition text-green-900 ">Lihat Detail</button>
                            </div>
                            {/if}
                            <!-- Card 2 -->
                            {#if giftRecommendations[i*2+1]}
                            <div class="w-64 h-72 flex flex-col items-center justify-between py-6">
                                <div class="flex-1 flex items-center justify-center">
                                    <div class="bg-neutral-400 w-40 h-40 flex items-center justify-center rounded-xl">
                                        {@html giftRecommendations[i*2+1].icon}
                                    </div>
                                </div>
                                <div class="text-neutral-50 text-lg mt-4 mb-1 text-center">{giftRecommendations[i*2+1].name}</div>
                                <button class="text-base sm:text-xl hover:border hover:border-lime-50 hover:bg-green-900 hover:text-lime-50 rounded-3xl bg-lime-50 sm:py-0.5 px-5 transition text-green-900 ">Lihat Detail</button>
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