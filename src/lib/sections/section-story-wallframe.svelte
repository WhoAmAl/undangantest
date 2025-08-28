<script lang="ts">
    import {
        Carousel,
        CarouselContent,
        CarouselItem,
        CarouselNext,
        CarouselPrevious
    } from "@/components/ui/carousel";
    // import * as Carousel from "$lib/components/ui/carousel/index.js";

    let slides = [
        {
            title: "Where It All Began",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "Where It All Began 2",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "Where It All Began 3",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "Where It All Began 4",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "Where It All Began 5",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
    ];

    import type { CarouselAPI } from "$lib/components/ui/carousel/context.js";
    let carouselapi = $state<CarouselAPI>();
    // const count = $derived(api ? api.scrollSnapList().length : 0);
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

<div class="min-h-screen sm:min-h-[1195px] flex px-3 pt-20 sm:pt-40 relative" style="font-family: 'Cormorant Garamond Regular';">
    <img src="/texturewallframe.png" alt="" class="w-full h-full absolute object-cover z-10">
    <div class="flex flex-col items-center bg-[#776B5D] w-[85%] sm:w-[60%] h-fit z-11">
        <img src="/texturewallframe.png" alt="" class="w-full h-full absolute object-cover z-10">
        <h1 class="text-center text-4xl py-8">Our Love Story</h1>
        <Carousel class="w-full relative z-101 items-center" setApi={handleCarouselAPI}>
            <CarouselContent>
                {#each slides as slide}
                    <CarouselItem class="z-101">
                        <div class="flex flex-col w-full h-fit px-3 md:px-5">
                            <h2 class="uppercase text-xl sm:text-[22px] text-left py-4 sm:pb-6" style="font-family: 'Julius Sans Regular';">{slide.title}</h2>
                            <p class="text-justify text-[16px] sm:text-[20.1px] font-light">
                                {slide.content}
                            </p>
                        </div>
                    </CarouselItem>
                {/each}
            </CarouselContent>
            <div class="flex justify-center mt-2 pb-5 w-[30%] mx-auto">
                <CarouselPrevious class="text-[#F3EEEA] border-0 hover:bg-[#F3EEEA] translate-y-0  translate-x-10 sm:h-[45px] sm:w-[45px] relative bg-[#B0A695]" />
                <CarouselNext     class="text-[#F3EEEA] border-0 hover:bg-[#F3EEEA] translate-y-0 -translate-x-10 sm:h-[45px] sm:w-[45px] relative bg-[#B0A695]" />
            </div>
        </Carousel>
    </div>

    <div class="absolute right-0 flex flex-col items-end -translate-y-5">
        <div class="sm:w-[100%]">
            <div class="bg-[#A29683]/30 w-full h-full absolute"></div>
            <img src="/storyimg1wallframe.png" alt="" class="w-full h-full object-cover">
        </div>

        <div class="w-[75%] mt-10 sm:w-[100%] sm:h-[30%] sm:mt-20 -translate-x-3">
            <div class="bg-[#A29683]/30 w-full h-full absolute"></div>
            <img src="/storyimg2wallframe.png" alt="" class="w-full h-full object-cover">
        </div>
    </div>

    <div class="absolute bottom-55 h-[25%] w-[40%] left-0 sm:w-[27%] sm:bottom-10 sm:h-[25%]">
        <div class="bg-[#A29683]/30 w-full h-full absolute"></div>
        <img src="/storyimg3wallframe.png" alt="" class="h-full w-full object-cover">
    </div>
</div>