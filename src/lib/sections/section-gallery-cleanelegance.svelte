<script lang="ts">
  import * as Carousel from "$lib/components/ui/carousel/index.js";

  import type { CarouselAPI } from "$lib/components/ui/carousel/context.js";
    let carouselapi = $state<CarouselAPI>();
    let current = $state(0);
    
    // Array of gallery items
    let galleryItems = [
        { id: 1, src: "/bgcovercleanelegance.png", alt: "Gallery Photo 1" },
        { id: 2, src: "/bgcovercleanelegance.png", alt: "Gallery Photo 2" },
        { id: 3, src: "/bgcovercleanelegance.png", alt: "Gallery Photo 3" },
        { id: 4, src: "/bgcovercleanelegance.png", alt: "Gallery Photo 4" },
        { id: 5, src: "/bgcovercleanelegance.png", alt: "Gallery Photo 5" }
    ];
    
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

<div class="bg-neutral-50">
    <!-- Content prime layout -->
    <div class="flex flex-col items-center">
        <div class="max-h-[290px] w-full">
            <div class="relative w-full h-full max-h-[290px] flex items-center justify-center">
                <img src="/livestreamcleanelegance.png" alt="" class="object-cover w-full h-full max-h-[290px]">
                <button class="absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 rounded-full p-3 hover:bg-black/80 transition z-10" aria-label="Play Video">
                    <svg class="w-full h-auto max-w-[39px]" viewBox="0 0 39 39" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
                        <path d="M34.7747 7.38404C31.2086 2.88617 25.6875 0 19.4998 0C8.7311 0 0 8.73204 0 19.5C0 30.2688 8.73196 39 19.4998 39C26.5847 39 32.7861 35.2211 36.1965 29.5704C37.9776 26.6322 39 23.1829 39 19.4991C39 14.923 37.4229 10.7103 34.775 7.38249L34.7747 7.38404ZM27.2094 20.5698L16.9593 27.9354C16.7325 28.0983 16.4677 28.184 16.1932 28.184C15.4652 28.184 14.8731 27.5923 14.8731 26.8653V12.1347C14.8731 11.4076 15.4651 10.8159 16.1932 10.8159C16.4681 10.8159 16.7328 10.9016 16.9593 11.0642L27.2094 18.4301C27.5531 18.6771 27.758 19.0772 27.758 19.4999C27.7577 19.923 27.5524 20.3226 27.2094 20.5698Z" fill="#FAFAFA" />
                    </svg>
                </button>
            </div>
        </div>
        <!-- second row pict -->
        <div class="w-full flex flex-col items-center gap-6 mt-6 px-3 sm:px-6">
            <!-- First row: 2 images -->
            <div class="flex flex-row gap-3 sm:gap-6 w-full justify-center">
                <img src="/bgcovercleanelegance.png" alt="Gallery 1" class="object-cover shadow-lg w-[210px] h-[270px] sm:w-[300px] sm:h-[370px]" />
                <img src="/bgcovercleanelegance.png" alt="Gallery 2" class="object-cover shadow-lg w-[210px] h-[270px] sm:w-[300px] sm:h-[370px]" />
            </div>
        </div>
        <!-- Bottom Images: Carousel Partial Slide -->
        <div class="mt-6 flex flex-row justify-center items-center w-full px-3 sm:px-6 overflow-x-hidden">
            <Carousel.Root class="w-full max-w-[900px]" setApi={handleCarouselAPI}>
                <Carousel.Content>
                    {#each galleryItems as item (item.id)}
                    <Carousel.Item class="basis-[220px] mx-2">
                        <div class="flex h-[290px] w-[220px] items-center justify-center overflow-hidden shadow">
                            <img src={item.src} alt={item.alt} class="w-full h-full object-cover" />
                        </div>
                    </Carousel.Item>
                    {/each}
                </Carousel.Content>
            </Carousel.Root>
        </div>
        <!-- Dot Pagination -->
        <div class="flex justify-center gap-2 md:gap-3 mt-10 mb-10">
            {#each galleryItems as _, index}
                <button
                    class="w-8 h-1.5 md:w-12 md:h-1.5 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                        {index === current - 1
                            ? 'bg-yellow-950 scale-110'
                            : 'bg-yellow-900 opacity-55 hover:bg-yellow-700 hover:scale-105'}"
                    onclick={() => carouselapi && carouselapi.scrollTo(index)}
                    aria-label={`Go to story ${index + 1}`}
                ></button>
            {/each}
        </div>
    </div>
</div>