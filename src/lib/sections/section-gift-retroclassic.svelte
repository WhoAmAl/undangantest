<script lang="ts">
  import * as Carousel from "$lib/components/ui/carousel/index.js";
</script>

<div class="bg-neutral-950 px-4 md:px-7 lg:px-10 min-h-screen sm:min-h-[165vh] xl:min-h-screen flex flex-col items-center" style="background-image: url(/landingopeningretroclassic.png); background-size: cover; background-position: center; background-repeat: no-repeat; font-family: 'Jomolhari', serif;">
	<!-- HeaDER -->
    <div class="w-full flex flex-col items-center justify-center text-neutral-50">
        <div class="w-full text-center pt-8">
            <div class="text-neutral-50 text-4xl lg:text-7xl tracking-[0.2em] mb-2" style="font-family: 'Jomolhari', serif;">GIFT</div>
            <div class="border-t-3 border-white w-full my-2"></div>
        </div>
        <p class="items-center justify-center text-center pt-2 md:pt-8 md:px-7 text-[22px]" style="font-family: 'Baskervville', serif;">If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful</p>
    </div>

    <!-- CONTENT BODY -->
     <div class="flex flex-col items-center w-full mt-5">
        <!-- CASHLESS & GIFT -->
        <div class="flex flex-col sm:flex-row w-full gap-4">
                <!-- Cashless -->
                <div class="bg-neutral-700/70 flex-1 flex flex-col items-center py-5">
                    <div class="text-white text-2xl font-serif tracking-widest mb-4" style="font-family: 'Baskervville', serif;">CASHLESS</div>
                    <!-- Rekening 1 -->
                    <div class="rounded-lg p-5 mb-4 w-full max-w-md flex flex-col items-center shadow-lg">
                        <img src="/creditcardwhiteskeleton.png" alt="Credit Card" width="48" height="48" class="mb-3" />
                        <div class="text-white text-lg mb-1">BCA a. n Hinata</div>
                        <div class="text-white text-2xl mb-3">123456789</div>
                        <button class="bg-white text-neutral-900 px-8 py-1.5 rounded-full hover:bg-neutral-200 transition" on:click={() => navigator.clipboard.writeText('123456789')}>Copy to clipboard</button>
                    </div>
                    <!-- Rekening 2 -->
                    <div class="rounded-lg p-5 w-full max-w-md flex flex-col items-center shadow-lg">
                        <img src="/creditcardwhiteskeleton.png" alt="Credit Card" width="48" height="48" class="mb-3" />
                        <div class="text-white text-lg mb-1">BCA a. n Naruto</div>
                        <div class="text-white text-2xl mb-3">123456789</div>
                        <button class="bg-white text-neutral-900 px-8 py-1.5 rounded-full hover:bg-neutral-200 transition" on:click={() => navigator.clipboard.writeText('123456789')}>Copy to clipboard</button>
                    </div>
                </div>
            <!-- Gift -->
            <div class="bg-neutral-700/70 flex-1 flex flex-col items-center justify-center">
                <div class="text-white text-3xl mb-1 sm:mb-4 pt-5 md:pt-0" style="font-family: 'Baskervville', serif;">GIFT</div>
                <div class="rounded-lg p-5 w-full max-w-md flex flex-col items-center">
                    <div class="text-white text-lg sm:text-2xl text-center px-6 mb-8" style="font-family: 'Baskervville', serif;">Orchid Streat Number 15, West Jakarta</div>
                    <button class="bg-white text-neutral-900 px-8 py-1.5 rounded-full hover:bg-neutral-200 transition" on:click={() => navigator.clipboard.writeText('Orchid Streat Number 15, West Jakarta')}>Copy address</button>
                </div>
            </div>
        </div>
        <!-- RECOMMENDED GIFT -->
        <div class="bg-neutral-700/70 w-full mt-4 py-4 flex flex-col items-center">
            <div class="text-white text-xl lg:text-2xl mb-1 text-center" style="font-family: 'Baskervville', serif;">GIFT RECOMMENDATION</div>
            <!-- Grid Cards: hanya tampil di sm ke atas -->
            <div class="hidden sm:flex flex-col sm:flex-row justify-center items-center w-full px-6">
                <!-- Card 1 -->
                <div class="rounded-xl w-64 h-72 flex flex-col items-center justify-between py-6">
                    <div class="flex-1 flex items-center justify-center">
                        <div class="bg-neutral-400 rounded-lg w-40 h-40 flex items-center justify-center">
                            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#888" viewBox="0 0 24 24"><path d="M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z"/></svg>
                        </div>
                    </div>
                    <div class="text-white text-lg mt-4 mb-1 text-center">Cermin</div>
                    <button class="bg-white text-neutral-900 px-7 py-1.5 rounded-2xl hover:bg-neutral-200 transition mb-2">Lihat Detail</button>
                </div>
                <!-- Card 2 -->
                <div class="rounded-xl w-64 h-72 flex flex-col items-center justify-between py-6">
                    <div class="flex-1 flex items-center justify-center">
                        <div class="bg-neutral-400 rounded-lg w-40 h-40 flex items-center justify-center">
                            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#888" viewBox="0 0 24 24"><path d="M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z"/></svg>
                        </div>
                    </div>
                    <div class="text-white text-lg mt-4 mb-1 text-center">Bedcover</div>
                    <button class="bg-neutral-50 text-neutral-900 px-7 py-1.5 rounded-2xl hover:bg-neutral-200 transition mb-2">Lihat Detail</button>
                </div>
                <!-- Card 3 -->
                <div class="rounded-xl w-64 h-72 flex flex-col items-center justify-between py-6">
                    <div class="flex-1 flex items-center justify-center">
                        <div class="bg-neutral-400 rounded-lg w-40 h-40 flex items-center justify-center">
                            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#888" viewBox="0 0 24 24"><path d="M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z"/></svg>
                        </div>
                    </div>
                    <div class="text-white text-lg mt-4 mb-1 text-center">Kulkas</div>
                    <button class="bg-neutral-50 text-neutral-900 px-7 py-1.5 rounded-2xl hover:bg-neutral-200 transition mb-2">Lihat Detail</button>
                </div>
            </div>
            <!-- Carousel: hanya tampil di bawah sm -->
            <div class="flex sm:hidden w-full px-2 mt-2 justify-center">
                <Carousel.Root>
                    <Carousel.Content class="flex justify-center">
                        <Carousel.Item>
                            <div class="rounded-xl mx-auto w-64 h-72 flex flex-col items-center justify-between py-6">
                                <div class="flex-1 flex items-center justify-center">
                                    <div class="bg-neutral-400 rounded-lg w-40 h-40 flex items-center justify-center">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#888" viewBox="0 0 24 24"><path d="M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z"/></svg>
                                    </div>
                                </div>
                                <div class="text-white text-lg mt-4 mb-1 text-center">Cermin</div>
                                <button class="bg-white text-neutral-900 px-7 py-1.5 rounded-2xl hover:bg-neutral-200 transition mb-2">Lihat Detail</button>
                            </div>
                        </Carousel.Item>
                        <Carousel.Item>
                            <div class="rounded-xl mx-auto w-64 h-72 flex flex-col items-center justify-between py-6">
                                <div class="flex-1 flex items-center justify-center">
                                    <div class="bg-neutral-400 rounded-lg w-40 h-40 flex items-center justify-center">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#888" viewBox="0 0 24 24"><path d="M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z"/></svg>
                                    </div>
                                </div>
                                <div class="text-white text-lg mt-4 mb-1 text-center">Bedcover</div>
                                <button class="bg-white text-neutral-900 px-7 py-1.5 rounded-2xl hover:bg-neutral-200 transition mb-2">Lihat Detail</button>
                            </div>
                        </Carousel.Item>
                        <Carousel.Item>
                            <div class="rounded-xl mx-auto w-64 h-72 flex flex-col items-center justify-between py-6">
                                <div class="flex-1 flex items-center justify-center">
                                    <div class="bg-neutral-400 rounded-lg w-40 h-40 flex items-center justify-center">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#888" viewBox="0 0 24 24"><path d="M21 19V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2zm-2 0H5V5h14zm-7-7l-2.5 3.01L7 12l-4 5h18z"/></svg>
                                    </div>
                                </div>
                                <div class="text-white text-lg mt-4 mb-1 text-center">Kulkas</div>
                                <button class="bg-white text-neutral-900 px-7 py-1.5 rounded-2xl hover:bg-neutral-200 transition mb-2">Lihat Detail</button>
                            </div>
                        </Carousel.Item>
                    </Carousel.Content>
                </Carousel.Root>
            </div>
        </div>
     </div>
</div>
