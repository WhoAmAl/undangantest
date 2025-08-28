<script lang="ts">
    import * as Carousel from "$lib/components/ui/carousel/index.js";

    let giftRecommendations = [
        {
            id:1,
            name: "Cermin",
            icon: "/gallerywallframe.png"
        },
        {
            id:2,
            name: "Bedcover",
            icon: "/gallerywallframe.png"
        },
        {
            id:3,
            name: "Kulkas",
            icon: "/gallerywallframe.png"
        },
        {
            id:4,
            name: "Kulkas",
            icon: "/gallerywallframe.png"
        },
        {
            id:5,
            name: "Kulkas",
            icon: "/gallerywallframe.png"
        },
        {
            id:6,
            name: "Kulkas",
            icon: "/gallerywallframe.png"
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

<div class="min-h-[1130px] relative pt-15 text-[#EBE3D5]" style="font-family: 'Cormorant Garamond Regular';">
    <img src="/texturewallframe.png" alt="" class="w-full h-full top-0 absolute object-cover z-2">
    <div class="absolute -top-5 sm:-top-10 right-0 h-[180px] sm:h-[374px] w-[265px] sm:w-[385px]">
        <div class="bg-[#A29683]/30 w-full h-full absolute"></div>
        <img src="/giftimg1wallframe.png" alt="" class="w-full h-full object-cover">
    </div>
    <div class="bg-[#776B5D] w-fit z-1 relative ml-auto mr-auto sm:mr-0 sm:ml-10 ">
        <h1 class="uppercase text-3xl sm:text-5xl px-10 py-4" style="font-family: 'Julius Sans Regular';">Wedding Gift</h1>
    </div>

    <div class="flex flex-col items-center bg-[#776B5D] z-3 relative sm:w-[437px] sm:ml-auto sm:mr-5 py-5 mt-8">
        <img src="/texturewallframe.png" alt="" class="w-full h-full top-0 absolute object-cover z-1">
        <p class="text-center text-xl px-8">If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful</p>
        <!-- card -->
        <div class="flex flex-col items-center mt-5">
            <h1 class="text-xl text-center leading-5" style="font-family: 'Cormorant Garamond Bold';">BCA</h1>
            <h2 class="text-xl text-center leading-5">Hinata</h2>
            <h3 class="text-xl text-center leading-5">12356789</h3>
            <button class="py-1 px-4 bg-[#B0A695] border border-[#B0A695] text-[#F3EEEA] mt-4 hover:bg-transparent transition z-2">Copy to Clipboard</button>
        </div>
        <div class="flex flex-col items-center mt-8">
            <h3 class="text-xl text-center leading-5 px-20">Orchid Streat Number 15, West Jakarta</h3>
            <button class="py-1 px-4 bg-[#B0A695] border border-[#B0A695] text-[#F3EEEA] mt-3 hover:bg-transparent transition z-2">Copy address</button>
        </div>
    </div>
    
    <div class="flex flex-col items-center text-center bg-[#776B5D] relative mt-4 sm:mt-10 ml-auto py-8 px-6 w-fit">
        <h1 class="text-2xl uppercase" style="font-family: 'Julius Sans Regular';">Gift Recommendation</h1>
    </div>

    <div class="hidden sm:block absolute right-0 -translate-y-6 h-[17%] w-[36%] bg-black">
        <div class="bg-[#A29683]/30 w-full h-full absolute"></div>
        <img src="/giftimg2wallframe.png" alt="" class="h-full w-full object-cover">
    </div>
    
    <div class="hidden sm:block absolute left-0 top-80 w-[55%] h-[25%] sm:h-[30%] sm:w-[42%] overflow-hidden z-4 shadow-2xl" style="background-image: url(/giftpict1wallframe.png); background-repeat: no-repeat; background-position: center;">
        <img src="/texturewallframe.png" alt="" class="w-full h-full top-0 absolute object-cover z-2">
        <div class="w-full h-full absolute bg-[#A29683]/30"></div>
        <img src="/giftframewallframe.png" alt="" class="h-full w-full object-cover object-right">
    </div>

    <div class="h-[242px] sm:w-[444px] bg-[#776B5D] z-3 relative sm:ml-15 mt-6 sm:mt-10 px-6 pt-4">
        <Carousel.Root class="w-full" setApi={handleCarouselAPI}>
            <Carousel.Content>
                {#each giftRecommendations as item (item.id)}
                <Carousel.Item class=" basis-[110px] mx-2 flex flex-col items-center">
                    <div class="flex h-[160px] w-[105px] items-center justify-center overflow-hidden shadow">
                        <div class="bg-[#A29683]/30 w-[105px] h-[160px] absolute"></div>
                        <img src={item.icon} alt={item.name} class="w-full h-full object-cover" />
                    </div>
                    <h1 class="text-center text-xs py-1">{item.name}</h1>
                    <button class="mx-auto px-2 text-xs bg-[#B0A695] border border-[#B0A695] text-[#F3EEEA] hover:bg-transparent transition">Check Detail</button>
                </Carousel.Item>
                {/each}
            </Carousel.Content>
        </Carousel.Root>
    </div>

    <div class="absolute bottom-0 left-0 w-[341px] h-[181px] z-3">
        <div class="bg-[#A29683]/30 w-full h-full absolute"></div>
        <img src="/giftimg3wallframe.png" alt="" class="w-full h-full object-cover">
    </div>
</div>  