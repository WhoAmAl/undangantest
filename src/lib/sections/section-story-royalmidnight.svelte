
<script lang="ts">
    import {
        Carousel,
        CarouselContent,
        CarouselItem,
    } from "@/components/ui/carousel";

    let slides = [
        {
            title: "WHERE IT ALL BEGAN 1",
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
        // Tambahkan slide lain di sini jika diperlukan
    ];

    import type { CarouselAPI } from "$lib/components/ui/carousel/context.js";
	import type { EmblaCarouselSvelteType } from "embla-carousel-svelte";
    let carouselapi = $state<CarouselAPI>();
    const count = $derived(api ? api.scrollSnapList().length : 0);
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

<div class="bg-[#172554] max-w-2xl h-[710px] mx-auto flex flex-col items-center relative">
    <div class="flex flex-col h-full w-full justify-between items-center" style="height:710px;">
        <div class="flex-1 flex flex-col justify-center">
            <h2 class="text-white text-2xl sm:text-3xl md:text-3xl tracking-[0.15em] sm:tracking-[0.2em] font-bold text-center font-[Cinzel]">OUR LOVE STORY</h2>
        </div>
        
        <!-- STORY CARDS as Carousel -->
        <Carousel class="w-full relative" setApi={handleCarouselAPI}>
            <CarouselContent>
                {#each slides as slide}
                    <CarouselItem>
                        <div class="bg-white flex flex-col justify-center items-center w-full max-w-[672px] min-h-[424px] h-fit">
                            <div class="flex flex-col justify-center items-center w-full h-full px-8 py-8" style="font-family: 'Cinzel', serif;">
                                <h3 class="text-[#172554] text-2xl font-bold mb-6 text-center tracking-wide" style="font-family: 'Cinzel', serif;">{slide.title}</h3>
                                <p class="text-[#172554] text-base sm:text-lg leading-relaxed text-center" style="font-family: 'Dancing Script', cursive;">
                                    {slide.content}
                                </p>
                            </div>
                        </div>
                    </CarouselItem>
                {/each}
            </CarouselContent>
        </Carousel>
        
        <!-- Dot Pagination -->
        <div class="flex justify-center gap-2 md:gap-3 mt-8 md:mt-10">
            {#each slides as _, index}
                <button
                    class="w-2 h-2 md:w-2.5 md:h-2.5 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                        {index === current - 1
                            ? 'bg-[#FBBF24] scale-110'
                            : 'bg-white hover:bg-gray-400 hover:scale-105'}"
                    onclick={() => api && api.scrollTo(index)}
                    aria-label={`Go to story ${index + 1}`}
                ></button>
            {/each}
        </div>
        <div class="flex-1"></div>
    </div>
</div>
