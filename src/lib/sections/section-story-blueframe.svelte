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

<div class="min-h-screen sm:min-h-[1195px] flex flex-col relative pt-2 sm:pt-5">
    <h1 class="uppercase text-3xl sm:text-5xl text-blue-950 w-fit text-center pl-5 sm:pl-10 sm:leading-20">Our Love <br><span class="uppercase text-4xl sm:text-[64px]" style="font-family: 'GFS Fleischman';">Story</span></h1>
    <div class="bg-blue-950 flex flex-col items-center ml-auto w-[365px] h-[509px] sm:w-[569px] sm:h-[559px] relative z-1 mt-5 sm:mt-15">
        <Carousel class="w-full text-center py-10" setApi={handleCarouselAPI}>
            <CarouselContent>
                {#each slides as slide}
                <CarouselItem>
                        <h1 class="text-2xl sm:text-4xl" style="font-family: 'GFS Fleischman';">Where It All Begin</h1>
                        <p class="text-lg sm:text-[19.8px] mt-5 px-5 sm:px-14">Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other. </p>
                    </CarouselItem>
                    {/each}
                </CarouselContent>
        </Carousel>
        <!-- pagination dot -->
        <div class="flex justify-center gap-2 md:gap-2 sm:mt-15 z-10">
            {#each slides as _, index}
                <button
                    class="w-[41px] h-[8px] sm:w-[41px] sm:h-[6px] transition-all duration-300 focus:outline-none focus:ring-2
                        {index === current - 1
                            ? 'bg-blue-900 scale-110'
                            : 'bg-blue-100 hover:bg-blue-700 hover:scale-105'}"
                    onclick={() => carouselapi && carouselapi.scrollTo(index)}
                    aria-label={`Go to story ${index + 1}`}
                ></button>
            {/each}
        </div>
    </div>

    <div class="absolute -bottom-5 sm:-bottom-10 left-0 w-[251px] h-[399px] sm:w-[371px] sm:h-[653px] z-0">
        <img src="img1storyblueframe.png" alt="" class="w-full h-full object-cover">
    </div>
    <div class="absolute -bottom-5 sm:-bottom-10 right-0 w-[145px] h-[262px] sm:w-[187px] sm:h-[325px] z-0">
        <img src="img2storyblueframe.png" alt="" class="w-full h-full object-cover">
    </div>
</div>