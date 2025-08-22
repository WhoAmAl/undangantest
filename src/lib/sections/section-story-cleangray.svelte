<script lang="ts">
    import {
        Carousel,
        CarouselContent,
        CarouselItem,
    } from "@/components/ui/carousel";

    let slides = [
        {
            title: "WHERE IT ALL BEGAN",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "WHERE IT ALL BEGAN 2",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "WHERE IT ALL BEGAN 3",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "WHERE IT ALL BEGAN 4",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "WHERE IT ALL BEGAN 5",
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

<div class="text-neutral-50" style="background-image: url(/covercleangray.png); background-size: cover; background-position: center; background-repeat: no-repeat;">
     <div class="flex flex-col text-center bg-slate-500/50 px-5 py-3">
        <h1 class="mb-2 sm:mb-5 text-5xl sm:text-6xl mt-5" style="font-family: 'Tangerine', cursive;">Our Love Story</h1>
        <div class="flex flex-row items-center justify-between">
            <div class="h-[110px] w-[110px] sm:h-[200px] sm:w-[200px]">
                <img src="/covercleangray.png" alt="" class="h-full w-full object-cover">
            </div>
            <div class="h-[110px] w-[110px] sm:h-[200px] sm:w-[200px]">
                <img src="/covercleangray.png" alt="" class="h-full w-full object-cover">
            </div>
            <div class="h-[110px] w-[110px] sm:h-[200px] sm:w-[200px]">
                <img src="/covercleangray.png" alt="" class="h-full w-full object-cover">
            </div>
        </div>

        <div class="w-full mt-5">
            <Carousel class="w-full relative z-0" setApi={handleCarouselAPI}>
                <CarouselContent>
                    {#each slides as slide}
                        <CarouselItem>
                            <div class="text-gray-50 flex flex-col items-center justify-center w-full h-fit px-1 md:px-5 md:py-1">
                                <h2 class="text-2xl sm:text-5xl text-center" style="font-family: 'Abhaya Regular';">{slide.title}</h2>
                                <p class="text-center text-[16px] sm:text-[26px] " style="font-family: 'Cormorant Garamond Regular';">
                                    {slide.content}
                                </p>
                            </div>
                        </CarouselItem>
                    {/each}
                </CarouselContent>
            </Carousel>
        </div>

        <!-- Dot Pagination -->
        <div class="flex justify-center gap-2 md:gap-2 mt-5 mb-5">
            {#each slides as _, index}
                <button
                    class="w-2 h-2 md:w-3 md:h-3 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                        {index === current - 1
                            ? 'bg-slate-700 scale-110'
                            : 'bg-slate-300 opacity-55 hover:bg-gray-700 hover:scale-105'}"
                    onclick={() => carouselapi && carouselapi.scrollTo(index)}
                    aria-label={`Go to story ${index + 1}`}
                ></button>
            {/each}
        </div>
    </div>
</div>