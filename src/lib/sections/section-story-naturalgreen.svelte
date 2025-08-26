<script lang="ts">
    import {
        Carousel,
        CarouselContent,
        CarouselItem,
    } from "@/components/ui/carousel";

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

<div class="flex flex-col items-center relative">
    <h1 class="mt-5 mb-5 text-3xl sm:text-5xl" style="font-family: 'Thank You Regular';">Our Love <span class="uppercase" style="font-family:'Hahmlet Regular';">Story</span></h1>

    <div class="w-full text-lime-50 px-6">
        <Carousel class="w-full relative z-0" setApi={handleCarouselAPI}>
            <CarouselContent>
                {#each slides as slide}
                    <CarouselItem>
                        <div class="bg-green-900 rounded-xl flex flex-col items-center justify-center w-full h-fit px-1 md:px-5 md:py-1">
                            <h2 class="text-xl sm:text-2xl text-center py-4 sm:py-6">{slide.title}</h2>
                            <p class="text-center text-[12px] sm:text-[19.9px] font-light pb-6 px-5">
                                {slide.content}
                            </p>
                        </div>
                    </CarouselItem>
                {/each}
            </CarouselContent>
        </Carousel>
    </div>

    <!-- Dot Pagination -->
        <div class="flex justify-center gap-2 md:gap-2 my-5 sm:my-15">
            {#each slides as _, index}
                <button
                    class="w-2 h-2 md:w-3 md:h-3 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                        {index === current - 1
                            ? 'bg-green-600 scale-110'
                            : 'bg-green-900 hover:bg-gray-700 hover:scale-105'}"
                    onclick={() => carouselapi && carouselapi.scrollTo(index)}
                    aria-label={`Go to story ${index + 1}`}
                ></button>
            {/each}
        </div>
</div>