<script lang="ts">
    import * as Carousel from "$lib/components/ui/carousel/index.js";

    let giftRecommendations = [
        {
            id:1,
            name: "Bedcover",
            icon: "/gallerygiftblueframe.png"
        },
        {
            id:2,
            name: "Bedcover",
            icon: "/gallerygiftblueframe.png"
        },
        {
            id:3,
            name: "Bedcover",
            icon: "/gallerygiftblueframe.png"
        },
        {
            id:4,
            name: "Kulkas",
            icon: "/gallerygiftblueframe.png"
        },
        {
            id:5,
            name: "Kulkas",
            icon: "/gallerygiftblueframe.png"
        },
        {
            id:6,
            name: "Kulkas",
            icon: "/gallerygiftblueframe.png"
        }
    ];

    import type { CarouselAPI } from "$lib/components/ui/carousel/context.js";

    let carouselapi = $state<CarouselAPI>();
    let current = $state(0);

    $effect(() => {
    if (carouselapi) {
        current = carouselapi.selectedScrollSnap() + 1;
        carouselapi.on("select", () => {
            current = carouselapi!.selectedScrollSnap() + 1;
        });
        }
    });

    function handleCarouselAPI (api: any) {
        carouselapi = api;
        if( !carouselapi ) {
            return; 
        }
        carouselapi.on("select", () => {
            current = carouselapi!.selectedScrollSnap();
        });
        current = carouselapi.selectedScrollSnap();
    }
</script>

<div class="min-h-screen sm:min-h-[1195px] relative pt-10" style="font-family: 'Questrial';">
    <div class="absolute w-[206px] h-[310px] sm:w-[322px] sm:h-[485px] top-0 -translate-y-15">
        <img src="/img1giftblueframe.png" alt="" class="w-full h-full object-cover">
    </div>
    <div class="absolute bottom-0 right-0 w-[201px] h-[337px] sm:w-[342px] sm:h-[498px]">
        <img src="/img2giftblueframe.png" alt="" class="w-full h-full object-cover">
    </div>

    <!-- main content -->
    <div class="bg-blue-950 py-7 sm:py-10 px-15 sm:px-20 relative z-1 w-fit ml-auto">
        <h1 class="uppercase text-3xl sm:text-4xl text-center" style="font-family: 'GFS Fleischman';">Wedding Gift</h1>
    </div>
    <h1 class="text-base sm:text-xl text-center ml-auto mt-2 sm:mt-10 text-blue-950 w-[197px] sm:w-[318px] mr-5 px-1 sm:px-5">If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful</h1>
    <div class="bg-blue-950 ml-auto sm:mx-auto w-[95%] sm:w-[80%] text-blue-100 z-1 relative flex flex-col py-5 sm:py-10 mt-4 sm:mt-6">
        <div class="flex flex-row items-center justify-between px-8 sm:px-15">
            <!-- card1 -->
            <div class="flex flex-col items-center">
                <svg width="41" height="31" viewBox="0 0 41 31" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M10.7082 20.375H16.5832C17.1026 20.375 17.6007 20.1687 17.9679 19.8014C18.3352 19.4342 18.5415 18.9361 18.5415 18.4167C18.5415 17.8973 18.3352 17.3992 17.9679 17.0319C17.6007 16.6647 17.1026 16.4584 16.5832 16.4584H10.7082C10.1888 16.4584 9.69068 16.6647 9.32342 17.0319C8.95616 17.3992 8.74984 17.8973 8.74984 18.4167C8.74984 18.9361 8.95616 19.4342 9.32342 19.8014C9.69068 20.1687 10.1888 20.375 10.7082 20.375ZM34.2082 0.791687H6.7915C5.23336 0.791687 3.73903 1.41066 2.63725 2.51243C1.53548 3.61421 0.916504 5.10854 0.916504 6.66669V24.2917C0.916504 25.8498 1.53548 27.3442 2.63725 28.4459C3.73903 29.5477 5.23336 30.1667 6.7915 30.1667H34.2082C35.7663 30.1667 37.2606 29.5477 38.3624 28.4459C39.4642 27.3442 40.0832 25.8498 40.0832 24.2917V6.66669C40.0832 5.10854 39.4642 3.61421 38.3624 2.51243C37.2606 1.41066 35.7663 0.791687 34.2082 0.791687ZM36.1665 24.2917C36.1665 24.8111 35.9602 25.3092 35.5929 25.6764C35.2257 26.0437 34.7276 26.25 34.2082 26.25H6.7915C6.27212 26.25 5.77401 26.0437 5.40675 25.6764C5.03949 25.3092 4.83317 24.8111 4.83317 24.2917V12.5417H36.1665V24.2917ZM36.1665 8.62502H4.83317V6.66669C4.83317 6.1473 5.03949 5.6492 5.40675 5.28194C5.77401 4.91468 6.27212 4.70835 6.7915 4.70835H34.2082C34.7276 4.70835 35.2257 4.91468 35.5929 5.28194C35.9602 5.6492 36.1665 6.1473 36.1665 6.66669V8.62502Z" 
                    fill="currentColor"/>
                </svg>
                <h1 class="text-lg">BCA an Sabrina</h1>
                <h2 class="text-lg leading-5">123456789</h2>
                <button class="mt-3 bg-blue-100 rounded-full text-blue-950 px-1 sm:px-6 py-0.5 border border-blue-100 hover:bg-transparent hover:text-blue-100 transition">Copy to Clipboard</button>
            </div>
            <!-- card2 -->
            <div class="flex flex-col items-center">
                <svg width="41" height="31" viewBox="0 0 41 31" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M10.7082 20.375H16.5832C17.1026 20.375 17.6007 20.1687 17.9679 19.8014C18.3352 19.4342 18.5415 18.9361 18.5415 18.4167C18.5415 17.8973 18.3352 17.3992 17.9679 17.0319C17.6007 16.6647 17.1026 16.4584 16.5832 16.4584H10.7082C10.1888 16.4584 9.69068 16.6647 9.32342 17.0319C8.95616 17.3992 8.74984 17.8973 8.74984 18.4167C8.74984 18.9361 8.95616 19.4342 9.32342 19.8014C9.69068 20.1687 10.1888 20.375 10.7082 20.375ZM34.2082 0.791687H6.7915C5.23336 0.791687 3.73903 1.41066 2.63725 2.51243C1.53548 3.61421 0.916504 5.10854 0.916504 6.66669V24.2917C0.916504 25.8498 1.53548 27.3442 2.63725 28.4459C3.73903 29.5477 5.23336 30.1667 6.7915 30.1667H34.2082C35.7663 30.1667 37.2606 29.5477 38.3624 28.4459C39.4642 27.3442 40.0832 25.8498 40.0832 24.2917V6.66669C40.0832 5.10854 39.4642 3.61421 38.3624 2.51243C37.2606 1.41066 35.7663 0.791687 34.2082 0.791687ZM36.1665 24.2917C36.1665 24.8111 35.9602 25.3092 35.5929 25.6764C35.2257 26.0437 34.7276 26.25 34.2082 26.25H6.7915C6.27212 26.25 5.77401 26.0437 5.40675 25.6764C5.03949 25.3092 4.83317 24.8111 4.83317 24.2917V12.5417H36.1665V24.2917ZM36.1665 8.62502H4.83317V6.66669C4.83317 6.1473 5.03949 5.6492 5.40675 5.28194C5.77401 4.91468 6.27212 4.70835 6.7915 4.70835H34.2082C34.7276 4.70835 35.2257 4.91468 35.5929 5.28194C35.9602 5.6492 36.1665 6.1473 36.1665 6.66669V8.62502Z" 
                    fill="currentColor"/>
                </svg>
                <h1 class="text-lg">BNI an Arthur</h1>
                <h2 class="text-lg leading-5">123456789</h2>
                <button class="mt-3 bg-blue-100 rounded-full text-blue-950 px-1 sm:px-6 py-0.5 border border-blue-100 hover:bg-transparent hover:text-blue-100 transition">Copy to Clipboard</button>
            </div>
        </div>
        <h1 class="text-lg sm:text-xl text-center mt-10 px-6 sm:px-20">Jalan Sudirman Kav 52-53, Kebayoran Baru, Senayan, Jakarta</h1>
        <button class="bg-blue-100 text-blue-950 border border-blue-100 hover:bg-transparent hover:text-blue-100 transition flex flex-row gap-3 mx-auto px-3 py-1 mt-5">
            <svg width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M20 12C20 17.018 14.5117 20.4027 12.9249 21.2764C12.6568 21.424 12.3432 21.424 12.0751 21.2764C10.4883 20.4027 5 17.018 5 12C5 7.5 8.63401 4.5 12.5 4.5C16.5 4.5 20 7.5 20 12Z" 
                    stroke="currentColor"/>
                    <circle cx="12.5" cy="12" r="3.5" 
                    stroke="currentColor"/>
                </svg>    
            Google Maps
        </button>
    </div>
    <h1 class="uppercase text-lg sm:text-2xl text-blue-950 w-[206px] sm:w-[326px] text-center mt-5 sm:mt-10 ml-3 sm:ml-0" style="font-family: 'GFS Fleischman';">Gift Recommendation</h1>
    <div class="bg-blue-950 w-[326px] h-[185px] sm:w-[533px] sm:h-[251px] flex items-center px-6 relative z-1 mt-10 bottom-5 sm:bottom-0">
        <Carousel.Root class="w-full" setApi={handleCarouselAPI}>
            <Carousel.Content>
                {#each giftRecommendations as item (item.id)}
                <Carousel.Item class="basis-[95px] sm:basis-[150px] mx-2 flex flex-col items-center">
                    <div class="flex w-[85px] h-[95px] sm:h-[144px] sm:w-[128px] items-center justify-center overflow-hidden shadow">
                        <img src={item.icon} alt={item.name} class="w-full h-full object-cover" />
                    </div>
                    <h1 class="text-center text-[16px] sm:text-lg py-1 sm:py-3">{item.name}</h1>
                    <button class="mx-auto px-1 py-0.5 text-xs bg-blue-100 border border-blue-100 text-blue-950 hover:bg-transparent hover:text-blue-100 transition">Check Detail</button>
                </Carousel.Item>
                {/each}
            </Carousel.Content>
        </Carousel.Root>
    </div>
</div>