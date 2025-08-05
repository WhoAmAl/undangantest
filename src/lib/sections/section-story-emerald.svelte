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

<svg class="w-0 h-0 absolute">
  <defs>
    <clipPath id="cover-clip" clipPathUnits="objectBoundingBox">
      <polygon points="
        0.5 0,
        1 0,
        1 0.9,
        0.87 0.95,
        0.7 0.99,
        0.52 1,
        0.33 0.99,
        0.15 0.95,
        0 0.9,
        0 0
      " />
    </clipPath>
  </defs>
</svg>

<div class="relative bg-[#042F2E] flex flex-col max-w-2xl mx-auto">
  <div class="absolute top-0 left-0 w-full" style="z-index:1;">
    <img
      src="/storyemerald.png"
      alt="Wedding Couple"
      class="object-cover w-full max-h-[370px] sm:max-h-[800px] sm:max-w-[100%]"
      style="clip-path: url(#cover-clip); object-position: top;"
      draggable="false"
    />
  </div>

<!-- Our Love Story Section -->
<div class="flex flex-col items-center justify-center pt-[270px] sm:pt-[500px] px-7 sm:px-15 text-center relative z-10">
  <h2 class="text-xl sm:text-4xl text-[#CA8A04] mb-4 sm:my-6" style="font-family: 'Emotional Use', cursive;">Our Love Story</h2>
      <div class="w-full max-w-3xl h-2 flex items-center sm:mb-5">
        <span class="w-4 h-4 bg-[#064E3B] rounded-full"></span>
        <!-- bar -->
        <span class="flex-1 h-1 bg-[#064E3B] rounded"></span>
        <span class="w-4 h-4 bg-[#064E3B] rounded-full"></span>
      </div>

  <!-- STORY CARDS as Carousel -->
  <Carousel class="w-full" setApi={handleCarouselAPI}>
      <CarouselContent>
          {#each slides as slide}
              <CarouselItem>
                  <div class="flex flex-col justify-center items-center w-full h-fit">
                      <div class="flex flex-col justify-center items-center w-full h-full py-8" style="font-family: 'Oblata-Regular', serif;">
                          <h3 class="text-[#CA8A04] text-lg sm:text-2xl mb-3 text-center tracking-wide">{slide.title}</h3>
                          <p class="text-[#FEF3C7] text-[14px] sm:text-lg leading-relaxed text-center">
                              {slide.content}
                          </p>
                      </div>
                  </div>
              </CarouselItem>
          {/each}
      </CarouselContent>
  </Carousel>

  <!-- Dot Pagination -->
  <div class="flex justify-center gap-2 md:gap-3 mt-8 md:mt-2 mb-55">
      {#each slides as _, index}
          <button
              class="w-2 h-2 md:w-2.5 md:h-2.5 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                  {index === current - 1
                      ? 'bg-[#FBBF24] scale-110'
                      : 'bg-white hover:bg-gray-400 hover:scale-105'}"
              onclick={() => carouselapi && carouselapi.scrollTo(index)}
              aria-label={`Go to story ${index + 1}`}
          ></button>
      {/each}
  </div>
</div>

</div>
