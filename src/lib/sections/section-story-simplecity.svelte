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

<div class="bg-[#6F7B95] flex flex-col items-center text-gray-200">
    <h1 class="text-4xl sm:text-5xl mt-10" style="font-family: 'Great Vibes Regular', serif;">Our Love Story</h1>
    <div class="w-[85%] flex flex-col justify-center mt-3 sm:mt-8 mb-10">
        <Carousel class="w-full relative z-0" setApi={handleCarouselAPI}>
            <CarouselContent>
                {#each slides as slide}
                    <CarouselItem>
                        <div class="text-gray-50 flex flex-col items-center justify-center w-full h-fit px-1 md:px-5 md:py-1">
                            <h2 class="text-2xl sm:text-3xl text-center">{slide.title}</h2>
                            <hr class="border-t-2 border-gray-200 w-full my-4">
                            <p class="text-center text-[16px] sm:text-[21.5px] ">
                                {slide.content}
                            </p>
                        </div>
                    </CarouselItem>
                {/each}
            </CarouselContent>
        </Carousel>
    </div>

     <!-- Dot Pagination -->
    <div class="flex justify-center gap-2 md:gap-2 mt-5 mb-15">
        {#each slides as _, index}
            <button
                class="w-8 h-1.5 md:w-8 md:h-1.5 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                    {index === current - 1
                        ? 'bg-[#223B59] scale-110'
                        : 'bg-gray-200 opacity-55 hover:bg-gray-700 hover:scale-105'}"
                onclick={() => carouselapi && carouselapi.scrollTo(index)}
                aria-label={`Go to story ${index + 1}`}
            ></button>
        {/each}
    </div>
</div>