<script lang="ts">
    import {
        Carousel,
        CarouselContent,
        CarouselItem,
    } from "@/components/ui/carousel";

    let slides = [
        {
            title: "First Time",
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

<div class="bg-neutral-50 flex flex-col justify-center items-center">
	<h1 class="leading-tight text-3xl md:text-5xl text-yellow-950 p-6" style="font-family: 'Tangerine Regular', serif;">Our Love Story</h1>
    <div class="flex flex-col justify-center items-center py-8 relative w-full" style="background-image: url(/storycleanelegance.png); background-size: cover; background-position: center; background-repeat: no-repeat;">
        <!-- Overlay untuk menutup background -->
        <div class="absolute inset-0 bg-neutral-100 opacity-40"></div>
        <div class="border-t-3 border-yellow-950 w-[90%] my-2 z-1"></div>
        <div class="w-full max-w-2xl px-2 md:px-5">
            <div class="pb-3 md:pb-3 px-2 md:px-8 text-center z-15">
                <Carousel class="w-full relative z-0" setApi={handleCarouselAPI}>
                    <CarouselContent>
                        {#each slides as slide}
                            <CarouselItem>
                                <div class="text-gray-50 flex flex-col items-center justify-center w-full h-fit sm:min-h-[320px] px-1 md:px-5 md:py-1">
                                    <div class="w-full px-5">
                                        <div class="bg-yellow-950 py-2 px-2 text-center w-full">
                                            <span class="text-xl md:text-4xl text-gray-50" style="font-family: 'Tangerine Regular', serif;">{slide.title}</span>
                                        </div>
                                    </div>
                                    <p class="text-center text-[14px] sm:text-[20.5px] mt-4 text-yellow-950 z-10">
                                        {slide.content}
                                    </p>
                                </div>
                            </CarouselItem>
                        {/each}
                    </CarouselContent>
                </Carousel>
            </div>
        </div>
        <div class="border-t-3 border-yellow-950 w-[90%] z-1"></div>
    </div>
     <!-- Dot Pagination -->
    <div class="flex justify-center gap-2 md:gap-3 mt-5 mb-15">
        {#each slides as _, index}
            <button
                class="w-8 h-1.5 md:w-10 md:h-2 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                    {index === current - 1
                        ? 'bg-yellow-950 scale-110'
                        : 'bg-yellow-900 opacity-55 hover:bg-yellow-700 hover:scale-105'}"
                onclick={() => carouselapi && carouselapi.scrollTo(index)}
                aria-label={`Go to story ${index + 1}`}
            ></button>
        {/each}
    </div>
</div>