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

<div class="relative">
    <div class="absolute translate-x-6 md:translate-x-16 -translate-y-14 md:-translate-y-18 text-4xl md:text-5xl text-lime-950" style="font-family: 'Rouge Script', serif;">
        <h1>
            Our Love Story
        </h1>
    </div>
    <!-- main content div -->
    <div class="bg-lime-900 mx-10 md:mx-22 mt-18 mb-10 md:min-h-[460px] flex flex-col justify-center rounded-tl-[100px] md:rounded-tl-[160px] rounded-br-[100px] md:rounded-br-[160px] md:pt-12 pb-4 md:pb-20 z-10 overflow-hidden" style="background-image: url(/backgroundbrideelegantlime.png); background-size: contain; background-position: center; background-repeat: no-repeat; background-attachment: fixed;">
        <!-- Carousel Content -->
        <Carousel class="w-full relative z-0" setApi={handleCarouselAPI}>
            <CarouselContent>
                {#each slides as slide}
                    <CarouselItem>
                        <div class="text-gray-50 flex flex-col items-center justify-center w-full h-fit min-h-[320px] px-8 md:px-10 md:py-5">
                            <h1 class="text-[14px] md:text-xl mb-5 text-center" style="font-family: 'Libre Caslon', serif;">
                                {slide.title}
                            </h1>
                            <p class="text-justify text-[12px] md:text-xl mt-4" style="font-family: 'Questrial', serif;">
                                {slide.content}
                            </p>
                        </div>
                    </CarouselItem>
                {/each}
            </CarouselContent>
        </Carousel>
    </div>

    <!-- Dot Pagination -->
        <div class="flex justify-center gap-2 md:gap-3 mb-15">
            {#each slides as _, index}
                <button
                    class="w-2 h-2 md:w-2.5 md:h-2.5 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                        {index === current - 1
                            ? 'bg-lime-900 scale-110'
                            : 'bg-lime-500 hover:bg-lime-700 hover:scale-105'}"
                    onclick={() => carouselapi && carouselapi.scrollTo(index)}
                    aria-label={`Go to story ${index + 1}`}
                ></button>
            {/each}
        </div>
</div>