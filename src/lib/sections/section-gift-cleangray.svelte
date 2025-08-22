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

<div class="text-neutral-50 flex flex-col items-center py-8 px-2 min-h-screen sm:min-h-[1195px] md:max-h-[1195px] relative overflow-hidden" style="background-image: url(/covercleangray.png); background-size: cover; background-position: center; background-repeat: no-repeat;">
    <div class="absolute inset-0 bg-slate-500/50"></div>
        <div class="relative text-center items-center justify-center flex flex-col">
            <h1 class="leading-tight text-3xl md:text-6xl p-2 md:p-6" style="font-family: 'Abhaya Regular';">GIFT</h1>
            <p class="text-base md:text-xl px-3 md:px-16">If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful</p>
        </div>
        <div class="border-t-2 border-neutral-50 w-[95%] my-2 relative"></div>
        <div class="flex flex-col items-center justify-center w-full relative">
            <!-- Digital money gift -->
            <div class="flex flex-col w-full items-center justify-center py-1 md:py-4">
                <!-- Card Icon di atas untuk <md -->
                <div class="text-neutral-50 flex flex-col items-center justify-center w-30 mb-2 md:hidden">
                    <svg 
                        class="w-24 h-16 md:w-32 md:h-20" 
                        viewBox="0 0 98 60" 
                        fill="none" 
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <mask id="mask0" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="0" y="0" width="98" height="60">
                            <path d="M0 0H98V59.8901H0V0Z" fill="white"/>
                        </mask>
                        <g mask="url(#mask0)">
                            <path 
                            d="M86.6785 41.2187C86.6785 40.5055 86.101 39.928 85.3891 39.928H77.4697C76.7565 39.928 76.179 40.5055 76.179 41.2187V49.1381C76.179 49.8488 76.7565 50.4263 77.4697 50.4263H85.3891C86.101 50.4263 86.6785 49.8488 86.6785 49.1381V41.2187ZM38.1345 48.0165H8.30789V50.4263H38.1345V48.0165ZM8.30789 42.3379H29.2859V39.928H8.30789V42.3379ZM97.9616 21.6955V52.9349C97.9616 56.712 94.9002 59.7733 91.1231 59.7733H6.87529C3.09823 59.7733 0.0380859 56.712 0.0380859 52.9349V21.6955H97.9616ZM97.9616 6.83649V12.0573H0.0380859V6.83649C0.0380859 3.06066 3.09823 -0.00195312 6.87529 -0.00195312H91.1231C94.9002 -0.00195312 97.9616 3.06066 97.9616 6.83649Z" 
                            fill="currentColor"
                            />
                        </g>
                    </svg>
                </div>
                <!-- Gift Cards -->
                <div class="flex flex-row items-center justify-center w-full gap-2 md:gap-4">
                    <!-- Gift Card 1 -->
                    <div class="flex flex-col items-center w-64">
                        <div class="text-neutral-50 text-center md:text-xl font-medium" style="font-family: 'Fleischman', serif;">BCA</div>
                        <div class="text-neutral-50 text-center md:text-lg" style="font-family: 'Cormorant Garamond Regular', serif;">1234567890</div>
                        <div class="text-neutral-50 text-center md:text-xl" style="font-family: 'Cormorant Garamond Regular', serif;">Hyuga Hinata</div>
                        <button class="text-base sm:text-xl hover:border hover:border-slate-700 rounded-3xl bg-slate-300 sm:py-0.5 px-5 transition text-slate-800 hover:shadow-[0_6px_0_0_rgba(51,65,85,1)]  active:shadow-[0_1px_0_0_rgba(51,65,85,1)] active:translate-y-1" style="font-family: 'Cormorant Garamond Regular', serif;" on:click={() => navigator.clipboard.writeText('1234567890')}>Copy to clipboard</button>
                    </div>
                    <!-- Card Icon untuk md+ -->
                    <div class="text-neutral-50 hidden md:flex flex-col items-center justify-center w-30 mb-2 md:mb-0">
                        <svg 
                        class="w-24 h-16 md:w-32 md:h-20" 
                        viewBox="0 0 98 60" 
                        fill="none" 
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <mask id="mask0" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="0" y="0" width="98" height="60">
                            <path d="M0 0H98V59.8901H0V0Z" fill="white"/>
                        </mask>
                        <g mask="url(#mask0)">
                            <path 
                            d="M86.6785 41.2187C86.6785 40.5055 86.101 39.928 85.3891 39.928H77.4697C76.7565 39.928 76.179 40.5055 76.179 41.2187V49.1381C76.179 49.8488 76.7565 50.4263 77.4697 50.4263H85.3891C86.101 50.4263 86.6785 49.8488 86.6785 49.1381V41.2187ZM38.1345 48.0165H8.30789V50.4263H38.1345V48.0165ZM8.30789 42.3379H29.2859V39.928H8.30789V42.3379ZM97.9616 21.6955V52.9349C97.9616 56.712 94.9002 59.7733 91.1231 59.7733H6.87529C3.09823 59.7733 0.0380859 56.712 0.0380859 52.9349V21.6955H97.9616ZM97.9616 6.83649V12.0573H0.0380859V6.83649C0.0380859 3.06066 3.09823 -0.00195312 6.87529 -0.00195312H91.1231C94.9002 -0.00195312 97.9616 3.06066 97.9616 6.83649Z" 
                            fill="currentColor"
                            />
                        </g>
                    </svg>
                    </div>
                    <!-- Gift Card 2 -->
                    <div class="flex flex-col items-center w-64 bg-transparent">
                        <div class="text-neutral-50 text-center md:text-xl font-medium" style="font-family: 'Fleischman', serif;">BCA</div>
                        <div class="text-neutral-50 text-center md:text-lg" style="font-family: 'Cormorant Garamond Regular', serif;">1234567890</div>
                        <div class="text-neutral-50 text-center md:text-xl" style="font-family: 'Cormorant Garamond Regular', serif;">Uzumaki Naruto</div>
                        <button class="text-base sm:text-xl hover:border hover:border-slate-700 rounded-3xl bg-slate-300 sm:py-0.5 px-5 transition text-slate-800 hover:shadow-[0_6px_0_0_rgba(51,65,85,1)]  active:shadow-[0_1px_0_0_rgba(51,65,85,1)] active:translate-y-1" style="font-family: 'Cormorant Garamond Regular', serif;" on:click={() => navigator.clipboard.writeText('1234567890')}>Copy to clipboard</button>
                    </div>
                </div>
            </div>
            <div class="border-t-2 border-neutral-50 w-[95%] my-2 relative"></div>
            <!-- Physical Gift -->
            <div class="flex flex-row items-center justify-center w-[95%] mb-2 py-2 md:mb-0">
                <!-- Icon -->
                <div class="text-neutral-50 flex items-center justify-center w-15 md:w-16 md:h-16 ml-6">
                    <svg width="64" height="64" viewBox="0 0 64 64" fill="none"
                            xmlns="http://www.w3.org/2000/svg">
                        <path d="M28.8 38.4007V64H16C13.4539 64 11.0121 62.9886 9.21178 61.1883C7.41143 59.388 6.4 56.9463 6.4 54.4003V41.6007C6.4 40.752 6.73714 39.9381 7.33726 39.338C7.93738 38.7379 8.75131 38.4007 9.6 38.4007H28.8ZM54.4 38.4007C55.2487 38.4007 56.0626 38.7379 56.6627 39.338C57.2629 39.9381 57.6 40.752 57.6 41.6007V54.4003C57.6 56.9463 56.5886 59.388 54.7882 61.1883C52.9879 62.9886 50.5461 64 48 64H35.2V38.4007H54.4ZM46.4 0.00187801C48.2896 0.00148801 50.1487 0.479197 51.804 1.39053C53.4594 2.30187 54.8572 3.61721 55.8674 5.2141C56.8776 6.81098 57.4674 8.63751 57.5818 10.5236C57.6962 12.4098 57.3314 14.2942 56.5216 16.0014H57.6C59.2974 16.0014 60.9253 16.6757 62.1255 17.8759C63.3257 19.0761 64 20.7039 64 22.4012V25.6011C64 27.2985 63.3257 28.9263 62.1255 30.1265C60.9253 31.3267 59.2974 32.0009 57.6 32.0009H35.2V16.0014H28.8V32.0009H6.4C4.70261 32.0009 3.07475 31.3267 1.87452 30.1265C0.674284 28.9263 0 27.2985 0 25.6011V22.4012C0 20.7039 0.674284 19.0761 1.87452 17.8759C3.07475 16.6757 4.70261 16.0014 6.4 16.0014H7.4784C6.76763 14.5012 6.39928 12.8617 6.4 11.2015C6.4 5.01613 11.4144 0.00187801 17.5456 0.00187801C23.1616 -0.0941192 28.144 3.49618 31.5648 9.3904L32 10.168C35.3056 4.04336 40.192 0.203472 45.7312 0.00827812L46.4 0.00187801ZM17.6 6.40169C16.327 6.40169 15.1061 6.90739 14.2059 7.80754C13.3057 8.70768 12.8 9.92855 12.8 11.2015C12.8 12.4746 13.3057 13.6954 14.2059 14.5956C15.1061 15.4957 16.327 16.0014 17.6 16.0014H27.6576C25.2864 9.90559 21.4208 6.33769 17.6 6.40169ZM46.3456 6.40169C42.5696 6.33769 38.7136 9.90879 36.3424 16.0014H46.4C47.673 15.9942 48.8911 15.4816 49.7861 14.5763C50.6812 13.6711 51.18 12.4474 51.1728 11.1743C51.1656 9.90135 50.653 8.68335 49.7477 7.7883C48.8424 6.89326 47.6186 6.39448 46.3456 6.40169Z" fill="currentColor"/>
                    </svg>

                </div>
                <div class="flex flex-col md:flex-row items-start md:items-center justify-center w-[95%] pl-5 py-2 gap-1 md:gap-4">
                    <!-- Address Info -->
                    <div class="flex flex-col justify-center flex-grow text-left md:px-4">
                        <div class="text-neutral-50 text-base md:text-xl" style="font-family: 'Cormorant Garamond Regular', serif;">Hinata &amp; Naruto</div>
                        <div class="text-neutral-50 text-xs md:text-xl" style="font-family: 'Cormorant Garamond Regular', serif;">Orchid Street Number 15, West Jakarta</div>
                    </div>
                    <!-- Copy Button -->
                    <button class="text-base sm:text-xl hover:border hover:border-slate-700 rounded-3xl bg-slate-300 sm:py-0.5 px-5 transition text-slate-800 hover:shadow-[0_6px_0_0_rgba(51,65,85,1)]  active:shadow-[0_1px_0_0_rgba(51,65,85,1)] active:translate-y-1" style="font-family: 'Cormorant Garamond Regular', serif;" on:click={() => navigator.clipboard.writeText('Orchid Street Number 15, West Jakarta')}>Copy address</button>
                </div>
            </div>
            <div class="border-t-2 border-neutral-50 w-[95%] relative"></div>
            <div class="relative text-center items-center justify-center flex flex-col">
                <h1 class="leading-tight text-lg md:text-4xl py-2 md:py-4" style="font-family: 'Abhaya Regular', serif;">Gift Recommendation</h1>
            </div>
            <div class="border-t-2 border-neutral-50 w-[95%] relative sm:mb-10"></div>
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
                        <div class="text-lg mt-1 text-center">{gift.name}</div>
                        <button class="text-base sm:text-xl hover:border hover:border-slate-700 rounded-3xl bg-slate-300 sm:py-0.5 px-5 transition text-slate-800 hover:shadow-[0_6px_0_0_rgba(51,65,85,1)]  active:shadow-[0_1px_0_0_rgba(51,65,85,1)] active:translate-y-1" style="font-family: 'Cormorant Garamond Regular';">
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
                                    <button class="text-base sm:text-xl hover:border hover:border-slate-700 rounded-3xl bg-slate-300 sm:py-0.5 px-5 transition text-slate-800 hover:shadow-[0_6px_0_0_rgba(51,65,85,1)]  active:shadow-[0_1px_0_0_rgba(51,65,85,1)] active:translate-y-1">Lihat Detail</button>
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
                                    <button class="text-base sm:text-xl hover:border hover:border-slate-700 rounded-3xl bg-slate-300 sm:py-0.5 px-5 transition text-slate-800 hover:shadow-[0_6px_0_0_rgba(51,65,85,1)]  active:shadow-[0_1px_0_0_rgba(51,65,85,1)] active:translate-y-1">Lihat Detail</button>
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