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
    ];

    import type { CarouselAPI } from "$lib/components/ui/carousel/context.js";
    let carouselapi = $state<CarouselAPI>();
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

<div class="bg-orange-100 flex flex-col items-center justify-between py-10 px-4 md:px-10 relative overflow-hidden max-w-2xl mx-auto">
  <!-- Ornamen Atas -->
  <div class="w-full flex justify-center px-1 md:px-10">
    <img src="/storytopmocavintage.png" alt="ornamen atas" class="w-full object-contain"/>
  </div>

  <!-- Judul -->
  <h2 class="text-2xl md:text-5xl font-serif text-yellow-950 opacity-80 tracking-wide text-center my-10" style="font-family: 'Fleischman', serif;">OUR LOVE STORY</h2>

  <!-- Carousel Story -->
  <div class="bg-[#7A5C3E] rounded-t-4xl px-4 md:px-6 max-w-2xl w-full mx-auto flex flex-col items-center shadow-md">
    <Carousel class="w-full" setApi={handleCarouselAPI}>
      <CarouselContent>
        {#each slides as slide}
          <CarouselItem>
            <div class="flex flex-col justify-center items-center w-full h-fit">
              <div class="flex flex-col justify-center items-center w-full h-full py-8">
                <h3 class="text-orange-100 text-2xl sm:text-2xl mb-3 text-center tracking-wide" style="font-family: 'Libre Caslon', serif;">{slide.title}</h3>
                <p class="text-orange-100 text-[14px] sm:text-lg leading-relaxed text-center" style="font-family: 'Foglihten', serif;">
                  {slide.content}
                </p>
              </div>
            </div>
          </CarouselItem>
        {/each}
      </CarouselContent>
    </Carousel>
  </div>

  <!-- Dot Pagination -->
  <div class="flex justify-center gap-2 md:gap-3 mt-8 md:mt-2 mb-10">
      {#each slides as _, index}
          <button
              class="w-2 h-2 md:w-2.5 md:h-2.5 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                  {index === current - 1
                      ? 'bg-lime-800 scale-110'
                      : 'bg-yellow-950 hover:bg-gray-800 hover:scale-105'}"
              onclick={() => carouselapi && carouselapi.scrollTo(index)}
              aria-label={`Go to story ${index + 1}`}
          ></button>
      {/each}
  </div>

  <!-- Ornamen Bawah -->
  <div class="w-full flex justify-center mt-0 px-1 md:px-10">
    <img src="/storybottommocavintage.png" alt="ornamen bawah" class="w-full object-contain" />
  </div>
</div>